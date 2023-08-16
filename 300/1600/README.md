# 1600 - Create the stories/Thing.stories.tsx file

Inside the root of the repository https://github.com/creations-global/frame/stories/, create a file called ```Thing.stories.tsx``` with the following content:

```
import React from 'react';
import { Meta, Story } from '@storybook/react';
import { Thing, Props } from '../src';

const meta: Meta = {
  title: 'Welcome',
  component: Thing,
  argTypes: {
    children: {
      control: {
        type: 'text',
      },
    },
  },
  parameters: {
    controls: { expanded: true },
  },
};

export default meta;

const Template: Story<Props> = args => <Thing {...args} />;

// By passing using the Args format for exported stories, you can control the props for a component for reuse in a test
// https://storybook.js.org/docs/react/workflows/unit-testing
export const Default = Template.bind({});

Default.args = {};
```
stories/Thing.stories.tsx
