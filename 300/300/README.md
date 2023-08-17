# 300 - Create the root package.json file

Inside the root of the repository https://github.com/creations-global/frame, create a file called ```package.json``` with the following content:

```
{
    "version": "0.1.0",
    "license": "MIT",
    "main": "dist/index.js",
    "repository": {
      "type": "git",
      "url": "https://github.com/creations-global/frame"
    },
    "bugs": {
      "url": "https://github.com/creations-global/frame"
    },
    "typings": "dist/index.d.ts",
    "files": [
      "dist",
      "src"
    ],
    "engines": {
      "node": ">=10"
    },
    "scripts": {
      "start": "tsdx watch",
      "build": "tsdx build",
      "commit": "git-cz",
      "test": "tsdx test --passWithNoTests",
      "lint": "tsdx lint",
      "prepare": "tsdx build",
      "size": "size-limit",
      "analyze": "size-limit --why",
      "storybook": "start-storybook -p 6006",
      "build-storybook": "build-storybook",
      "semantic-release": "semantic-release --branches main"
    },
    "peerDependencies": {
      "react": ">=16"
    },
    "husky": {
      "hooks": {
        "pre-commit": "tsdx lint",
        "prepare-commit-msg": "exec < /dev/tty && npx cz --hook || true"
      }
    },
    "prettier": {
      "printWidth": 80,
      "semi": true,
      "singleQuote": true,
      "trailingComma": "es5"
    },
    "name": "@creations_global/frame",
    "author": "Willem van Heemstra",
    "module": "dist/frame.esm.js",
    "size-limit": [
      {
        "path": "dist/frame.cjs.production.min.js",
        "limit": "10 KB"
      },
      {
        "path": "dist/frame.esm.js",
        "limit": "10 KB"
      }
    ],
    "devDependencies": {
      "@babel/core": "^7.21.4",
      "@size-limit/preset-small-lib": "^8.2.4",
      "@storybook/addon-essentials": "^7.0.2",
      "@storybook/addon-info": "^4.1.18",
      "@storybook/addon-links": "^7.0.2",
      "@storybook/addons": "^7.0.2",
      "@storybook/react": "^7.0.2",
      "@types/react": "^18.0.33",
      "@types/react-dom": "^18.0.11",
      "babel-loader": "^9.1.2",
      "commitizen": "4.3.0",
      "husky": "^8.0.3",
      "react": "^18.2.0",
      "react-dom": "^18.2.0",
      "react-is": "^18.2.0",
      "semantic-release": "^21.0.1",
      "semantic-release-cli": "^5.4.4",
      "size-limit": "^8.2.4",
      "tsdx": "^0.13.3",
      "tslib": "^2.5.0",
      "typescript": "^5.0.3"
    },
    "publishConfig": {
      "access": "public"
    }
  }
```
package.json

**NOTE**: Pay close attention, the **name** in the above package.json is ```"name": "@creations_global/frame"```, instead of ```creations-global```, as this is the name that was available at the time of registration with npm.
