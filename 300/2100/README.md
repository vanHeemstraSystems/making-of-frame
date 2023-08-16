# 2100 - Create files in example/

## 100 - .npmignore

Inside the repository https://github.com/creations-global/frame/example/, create a file called ```.npmignore``` with the following content:

```
node_modules
.cache
dist
```
example/.npmignore

## 200 - index.tsx

Inside the repository https://github.com/creations-global/frame/example/, create a file called ```index.tsx``` with the following content:

```
import 'react-app-polyfill/ie11';
import * as React from 'react';
import * as ReactDOM from 'react-dom';
import { Thing } from '../.';

const App = () => {
  return (
    <div>
      <Thing />
    </div>
  );
};

ReactDOM.render(<App />, document.getElementById('root'));
```
example/index.tsx

## 300 - index.html

Inside the repository https://github.com/creations-global/frame/example/, create a file called ```index.html``` with the following content:

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Playground</title>
  </head>

  <body>
    <div id="root"></div>
    <script src="./index.tsx"></script>
  </body>
</html>
```
example/index.html

## 400 - package.json

Inside the repository https://github.com/creations-global/frame/example/, create a file called ```package.json``` with the following content:

```
{
    "name": "example",
    "version": "1.0.0",
    "main": "index.js",
    "license": "MIT",
    "scripts": {
      "start": "parcel index.html",
      "build": "parcel build index.html"
    },
    "dependencies": {
      "react-app-polyfill": "^1.0.0"
    },
    "alias": {
      "react": "../node_modules/react",
      "react-dom": "../node_modules/react-dom/profiling",
      "scheduler/tracing": "../node_modules/scheduler/tracing-profiling"
    },
    "devDependencies": {
      "@types/react": "^16.9.11",
      "@types/react-dom": "^16.8.4",
      "parcel": "^1.12.3",
      "typescript": "^3.4.5"
    }
}
```
example/package.json

## 500 - tsconfig.json

Inside the repository https://github.com/creations-global/frame/example/, create a file called ```tsconfig.json``` with the following content:

```
{
    "compilerOptions": {
      "allowSyntheticDefaultImports": false,
      "target": "es5",
      "module": "commonjs",
      "jsx": "react",
      "moduleResolution": "node",
      "noImplicitAny": false,
      "noUnusedLocals": false,
      "noUnusedParameters": false,
      "removeComments": true,
      "strictNullChecks": true,
      "preserveConstEnums": true,
      "sourceMap": true,
      "lib": ["es2015", "es2016", "dom"],
      "types": ["node"]
    }
}
```
example/tsconfig.json
