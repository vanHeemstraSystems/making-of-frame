# 1700 - Create the test/blah.test.tsx file

Inside the root of the repository https://github.com/creations-global/frame/test/, create a file called ```blah.test.tsx``` with the following content:

```
import React from 'react';
import * as ReactDOM from 'react-dom';
import { Default as Thing } from '../stories/Thing.stories';

describe('Thing', () => {
  it('renders without crashing', () => {
    const div = document.createElement('div');
    ReactDOM.render(<Thing />, div);
    ReactDOM.unmountComponentAtNode(div);
  });
});
```
test/blah.test.tsx
