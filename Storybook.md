Storybook – 
 
Storybook is an open-source tool for building and showcasing UI components in isolation. It provides a development environment where you can create and document individual components outside of your application, making it easier to develop, test, and showcase your user interface.
Storybook is widely used in web development to improve component-driven development and documentation. It is especially helpful in large-scale projects and design systems where there are numerous UI components that need to be developed and showcased systematically
Latest version as of 21/10/23 is 7.5,  Kadira was the original developer of Storybook. Kadira was a bootstrapped Sri Lankan startup, in April 2016 led by Arunoda Susirapala and consisting of a talented and close-knit team of developers.
1.	Storybook 1.0 was developed by a startup called Kadira and launched in April 2016.
2.	Storybook 2.0 was released by Kadira in September 2016 with great docs, extensibility, and a paid hosted service.
3.	Kadira shut down in December 2016 and Storybook development went idle from mid-January 2017.
4.	After a minor uproar on Github in April 2017, the project was handed off to the community.
5.	Storybook 3.0 was released in May 2017, driven by the community.

Key features and use cases of Storybook include:
•	Component Showcase: Storybook allows you to create a catalog of your UI components, making it easy to browse and interact with them independently.
•	Interactive (props and Documentation)
•	Component Testing: 
•	Supported Frameworks.
•	Addons: Storybook supports a wide range of addons that extend its functionality. These include knobs, actions, backgrounds, and many more to enhance the development and documentation experience.

// Button.stories.ts
import type { Meta, StoryObj } from '@storybook/react';

import { Button } from './Button';

// More on how to set up stories at: https://storybook.js.org/docs/react/writing-stories/introduction#default-export
const meta = {
  title: 'Example/Button',
  component: Button,
  parameters: {
    // Optional parameter to center the component in the Canvas. More info: https://storybook.js.org/docs/react/configure/story-layout
    layout: 'centered',
  },
  // This component will have an automatically generated Autodocs entry: https://storybook.js.org/docs/react/writing-docs/autodocs
  tags: ['autodocs'],
  // More on argTypes: https://storybook.js.org/docs/react/api/argtypes
  argTypes: {
    backgroundColor: { control: 'color' },
  },
} satisfies Meta<typeof Button>;

export default meta;
type Story = StoryObj<typeof meta>;

// More on writing stories with args: https://storybook.js.org/docs/react/writing-stories/args
export const Primary: Story = {
  args: {
    primary: true,
    label: 'Button',
  },
};

export const Secondary: Story = {
  args: {
    label: 'Button',
  },
};

export const Large: Story = {
  args: {
    size: 'large',
    label: 'Button',
  },
};

export const Small: Story = {
  args: {
    size: 'small',
    label: 'Button',
  },
};


The “Docs” page displays auto-generated documentation for components (inferred from the source code). Usage documentation is helpful when sharing reusable components with your team.

How to write a story
Imports
First, import Meta and StoryObj for type safety and autocompletion in TypeScript stories.
Next, import a component. In this case, the Button component.

Meta
The default export, Meta, contains metadata about this component's stories. The title field (optional) controls where stories appear in the sidebar.

Story
Each named export is a story. Its contents specify how the story is rendered in addition to other configuration options.

Addons
Addons are plugins that extend Storybook's core functionality. You can find them in the addons panel, a reserved place in the Storybook UI below the Canvas. Each tab shows the generated metadata, logs, or static analysis for the selected story by the addon.
Controls allows you to interact with a component’s args (inputs) dynamically. 
Actions help you verify interactions produce the correct outputs via callbacks. 
Interactions provides a helpful user interface for debugging interaction tests with the play function.
Storybook is extensible. Our rich ecosystem of addons helps you test, document, and optimize your stories. You can also create an addon to satisfy your workflow requirements. Read more in the addons section.

Render component styles
Storybook isn’t opinionated about how you generate or load CSS. It renders whatever DOM elements you provide. But sometimes, things won’t “look right” out of the box.
You may have to configure your CSS tooling for Storybook’s rendering environment. Here are some setup guides for popular tools in the community.

Tailwind
Material UI
Vuetify
Styled Components
Emotion
Sass
Bootstrap
Less
Vanilla-extract

Where to put stories - 
A component’s stories are defined in a story file that lives alongside the component file. The story file is for development-only, and it won't be included in your production bundle.

Button.js | ts | jsx | tsx | vue | svelte
Button.stories.js | ts | jsx | tsx

Component Story Format - 
We define stories according to the Component Story Format (CSF), an ES6 module-based standard that is easy to write and portable between tools.

The key ingredients are the default export that describes the component, and named exports that describe the stories.

Working with React Hooks
React Hooks are convenient helper methods to create components using a more streamlined approach. You can use them while creating your component's stories if you need them, although you should treat them as an advanced use case. We recommend args as much as possible when writing your own stories. 

Args - 
A story is a component with a set of arguments that define how the component should render. “Args” are Storybook’s mechanism for defining those arguments in a single JavaScript object. Args can be used to dynamically change props, slots, styles, inputs, etc. It allows Storybook and its addons to live edit components. You do not need to modify your underlying component code to use args.

When an arg’s value changes, the component re-renders, allowing you to interact with components in Storybook’s UI via addons that affect args.

Args object -
The args object can be defined at the story, component and global level. It is a JSON serializable object composed of string keys with matching valid value types that can be passed into a component for your framework.

Setting args through the URL -
You can also override the set of initial args for the active story by adding an args query parameter to the URL. Typically you would use the Controls addon to handle this.
?path=/story/avatar--default&args=style:rounded;size:100
As a safeguard against XSS attacks, the arg's keys and values provided in the URL are limited to alphanumeric characters, spaces, underscores, and dashes. Any other types will be ignored and removed from the URL, but you can still use them with the Controls addon and within your story.

argTypes -

argTypes is an option used in the story configuration for a component. It's used to control and customize the behavior of the Component Story Format (CSF) in Storybook. The argTypes object allows you to define the types, initial values, and other metadata for the arguments (or props) of your component stories. This can be helpful for documentation, controlling component behavior, and even generating controls in the Storybook UI for interactive component testing.

argTypes: {
    backgroundColor: {
      control: 'color',
      name: 'Background Color',
      description: 'The background color of the component',
      defaultValue: '#FFFFFF',
      table: {
        type: { summary: 'string' },
      },
      options: ['red', 'blue', 'green'],
      mapping: {
        red: 'Red',
        blue: 'Blue',
        green: 'Green',
      },
      disable: false,
    },
  }

Parameters -
Parameters are a set of static, named metadata about a story, typically used to control the behavior of Storybook features and addons.

In Storybook, "parameters" are special configuration options that you can use to customize the behavior and appearance of your stories. They allow you to fine-tune how your stories are presented, documented, and interacted with in the Storybook UI. Parameters are typically defined at the story level, but you can also define them globally for your entire Storybook.

parameters: {
    backgrounds: {
      default: 'light',
      values: [
        { name: 'light', value: '#FFFFFF' },
        { name: 'dark', value: '#000000' },
      ],
    },
    actions: { argTypesRegex: '^on.*' },
    controls: { expanded: true },
    docs: {
      description: {
        component: 'A customizable button component.',
      },
    },
  },

Rules of parameter inheritance -
The way the global, component and story parameters are combined is:

More specific parameters take precedence (so a story parameter overwrites a component parameter which overwrites a global parameter).
Parameters are merged so keys are only ever overwritten, never dropped.
The merging of parameters is important. It means it is possible to override a single specific sub-parameter on a per-story basis but still retain the majority of the parameters defined globally.

Decorator -
A decorator is a way to wrap a story in extra “rendering” functionality. 
When writing stories, decorators are typically used to wrap stories with extra markup or context mocking.
Like other addons, decorators can be defined globally, at the component level, and for a single story (as we’ve seen).

Wrap stories with extra markup –
const meta: Meta<typeof YourComponent> = {
  component: YourComponent,
  decorators: [
    (Story) => (
      <div style={{ margin: '3em' }}>
        {/* 👇 Decorators in Storybook also accept a function. Replace <Story/> with Story() to enable it  */}
        <Story />
      </div>
    ),
  ],
};

“Context” for mocking -
const preview: Preview = {
    decorators: [
      (Story) => (
        <ThemeProvider theme="default">
          {/* 👇 Decorators in Storybook also accept a function. Replace <Story/> with Story() to enable it  */}
          <Story />
        </ThemeProvider>
      ),
    ],
  };

Using decorators to provide data -
If your components are “connected” and require side-loaded data to render, you can use decorators to provide that data in a mocked way without having to refactor your components to take that data as an arg. There are several techniques to achieve this. Depending on exactly how you are loading that data -- read more in the building pages in Storybook section.



Play –
Play functions are small snippets of code executed after the story renders. Enabling you to interact with your components and test scenarios that otherwise required user intervention.
When Storybook finishes rendering the story, it executes the steps defined within the play function, interacting with the component without the need for user intervention.

Working with events
A common type of component interaction is a button click. 
export const ClickExample: Story = {
  play: async ({ canvasElement }) => {
    const canvas = within(canvasElement);

    // See https://storybook.js.org/docs/react/essentials/actions#automatically-matching-args to learn how to setup logging in the Actions panel
    await userEvent.click(canvas.getByRole('button'));
  },
};

// Starts querying from the component's root element
    await userEvent.type(canvas.getByTestId('example-element'), 'something');
    await userEvent.click(canvas.getByRole('another-element'));
    await userEvent.type(emailInput, 'example-email@email.com', {
        delay: 100,
      });

Loaders -
Loaders are asynchronous functions that load data for a story and its decorators. A story's loaders run before the story renders, and the loaded data injected into the story via its render context.
Loaders can be used to load any asset, lazy load components, or fetch data from a remote API. This feature was designed as a performance optimization to handle large story imports. However, args is the recommended way to manage story data. We're building up an ecosystem of tools and techniques around Args that might not be compatible with loaded data.
All loaders, defined at all levels that apply to a story, run before the story renders in Storybook's canvas.
•	All loaders run in parallel
•	All results are the loaded field in the story context

loaders: [
    async () => ({
      todo: await (await fetch('https://jsonplaceholder.typicode.com/todos/1')).json(),
    }),
  ],

Structure and hierarchy
When organizing your Storybook, there are two methods of structuring your stories: implicit and explicit. The implicit method involves relying upon the physical location of your stories to position them in the sidebar, while the explicit method involves utilizing the title parameter to place the story.

 


Grouping
It is also possible to group related components in an expandable interface to help with Storybook organization.

Sorting stories
Out of the box, Storybook sorts stories based on the order in which they are imported. However, you can customize this pattern to suit your needs and provide a more intuitive experience by adding storySort to the options parameter in your preview.js file.

const preview: Preview = {
  parameters: {
    options: {
      storySort: (a, b) =>
        a.id === b.id ? 0 : a.id.localeCompare(b.id, undefined, { numeric: true }),
    },
  },
};

const preview: Preview = {
  parameters: {
    options: {
      storySort: {
        method: '',
        order: [],
        locales: '',
      },
    },
  },
};

const preview: Preview = {
  parameters: {
    options: {
      storySort: {
        order: ['Intro', 'Pages', ['Home', 'Login', 'Admin'], 'Components'],
      },
    },
  },
};

Note that the order option is independent of the method option; stories are sorted first by the order array and then by either the method: 'alphabetical' or the default configure() import order.

Field	Type	Description	Required	Default Value	Example
method	String	Tells Storybook in which order the stories are displayed	No	Storybook configuration	'alphabetical'
order	Array	The stories to be shown, ordered by supplied name	No	Empty Array []	['Intro', 'Components']
includeNames	Boolean	Include story name in sort calculation	No	false	true
locales	String	The locale required to be displayed	No	System locale	en-US

Automatic documentation and Storybook

Storybook Autodocs is a powerful tool that can help you quickly generate comprehensive documentation for your UI components. By leveraging Autodocs, you're transforming your stories into living documentation which can be further extended with MDX and Doc Blocks to provide a clear and concise understanding of your components' functionality.

To enable auto-generated documentation for your stories –
Option	Description
autodocs	Configures auto-generated documentation pages. Available options: true, false,tag (default). true/false enable/disable autodocs globally. tag allows you to opt in per component by adding the tags: ['autodocs'] annotation in the component's default export.
Default: docs: { autodocs: 'tag' }
defaultName	Renames the auto-generated documentation page
Default: docs: { defaultName: 'Documentation' }

Args composition for presentational screens – 

When you are building screens in this way, it is typical that the inputs of a composite component are a combination of the inputs of the various sub-components it renders.
In such cases, it is natural to use args composition to build the stories for the page based on the stories of the sub-components:
This approach is beneficial when the various subcomponents export a complex list of different stories.



// YourPage.stories.ts|tsx

// Replace your-framework with the name of your framework
import type { Meta, StoryObj } from '@storybook/your-framework';

import { DocumentScreen } from './YourPage';

// 👇 Imports the required stories
import * as PageLayout from './PageLayout.stories';
import * as DocumentHeader from './DocumentHeader.stories';
import * as DocumentList from './DocumentList.stories';

const meta: Meta<typeof DocumentScreen> = {
  component: DocumentScreen,
};

export default meta;
type Story = StoryObj<typeof DocumentScreen>;

export const Simple: Story = {
  args: {
    user: PageLayout.Simple.args.user,
    document: DocumentHeader.Simple.args.document,
    subdocuments: DocumentList.Simple.args.documents,
  },
};

Learn more about Storybook documentation
•	Autodocs for creating documentation for your stories
•	MDX for customizing your documentation
•	Doc Blocks for authoring your documentation
•	Publishing docs to automate the process of publishing your documentation

MDX and CSF
The first thing you'll notice is that the component documentation is divided into distinct formats: one for writing component stories describing each possible component state and the second one for documenting how to use them. This split leverages the best qualities of each format:
•	CSF is great for succinctly defining stories (component examples). If you use TypeScript, it also provides type safety and auto-completion.
•	MDX is great for writing structured documentation and composing it with interactive JSX elements.

Mocking connected components -
Mocking providers - 
Suppose you are using a provider that supplies data via the context. In that case, you can wrap your story in a decorator that provides a mocked version of that provider.
Mocking API Services -
Suppose you're working in an application that relies on REST or GraphQL endpoints data providers. In that case, you can add Mock Service Worker (MSW) via Storybook's MSW addon to mock data alongside your app and stories.
Mock Service Worker is an API mocking library. It relies on service workers to capture network requests and provides mocked data in response. The MSW addon adds this functionality into Storybook, allowing you to mock API requests in your stories.
>npm install msw msw-storybook-addon --save-dev
