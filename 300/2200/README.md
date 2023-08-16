# 2200 - Create files in .storybook/

## 100 - main.js

Inside the repository https://github.com/creations-global/frame/.storybook/, create a file called ```main.js``` with the following content:

```
module.exports = {
    stories: ['../stories/**/*.stories.@(ts|tsx|js|jsx)'],
    addons: ['@storybook/addon-links', '@storybook/addon-essentials'],
    // https://storybook.js.org/docs/react/configure/typescript#mainjs-configuration
    typescript: {
      check: true, // type-check stories during Storybook build
    }
};
```
.storybook/main.js

## 200 - preview.js

Inside the repository https://github.com/creations-global/frame/.storybook/, create a file called ```preview.js``` with the following content:

```
// https://storybook.js.org/docs/react/writing-stories/parameters#global-parameters
export const parameters = {
    // https://storybook.js.org/docs/react/essentials/actions#automatically-matching-args
    actions: { argTypesRegex: '^on.*' },
};
```
.storybook/preview.js
