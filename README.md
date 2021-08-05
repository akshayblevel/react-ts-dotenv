# react-ts-dotenv

.env.dev

REACT_APP_APIBASEURL=https://607050b585c3f0001746fd55.mockapi.io/crud

endpointUrlConstant.ts

```js
export const API_URL_CONSTANT = {
  EMPLOYEE_LIST: `${process.env.REACT_APP_APIBASEURL}/employee`,
  EMPLOYEE_NEW: `${process.env.REACT_APP_APIBASEURL}/employee`
};
```

app.tsx

```js
import React from 'react';
import { API_URL_CONSTANT } from './constant/endpointUrlConstant';

function App() {
  return <div>Environment Config Value: {API_URL_CONSTANT.EMPLOYEE_NEW}</div>;
}

export default App;
```

package.json

```js
"scripts": {
    "start": "react-scripts-ts start",
    "build": "react-scripts-ts build",
    "start:dev": "env-cmd -f .env.dev react-scripts start",
    "build:dev": "env-cmd -f .env.dev react-scripts build",
    "test": "react-scripts-ts test --env=jsdom",
    "eject": "react-scripts-ts eject"
  },
```

Run application

  npm run start:dev

Build application

  npm run build:dev

