## React App with Typescript

You want to use TypeScript in React but you’re not sure how to start. You’ve come to the right place!

![image](https://github.com/2211rohit/react-with-typescript/assets/53754318/a53830e7-6ce9-44f7-b14f-373ebf567f82)


# New App from Scratch
If you’re building a new app and using create-react-app, the Create React App docs are great:

You can start a new TypeScript app using templates. To use our provided TypeScript template, append `--template typescript` to the creation command.

```npx create-react-app my-app --template typescript```

It compiles beautifully with no special settings to enable or packages to download. All the files that would have been `.js` files are now `.ts` or `.tsx`.

![image](https://github.com/2211rohit/react-with-typescript/assets/53754318/d6864567-0767-439e-803f-c121feebb032)


If you’ve found yourself in the situation where you’ve already gotten started on a project and want to convert to TypeScript, not to worry! There’s a solution for that too.

# Converting an Existing App to TypeScript
In the terminal, navigate to your app directory, where you’ll want to install TypeScript:

```
npm install --save typescript @types/node @types/react @types/react-
dom @types/jest
```

Then rename any files you would like to be TypeScript files to end in `.tsx`. For example, `App.tsx`, instead of `App.js`.

Here’s where you might run into issues. If you open your `App.tsx` file, you’ll see that almost everything is underlined in red. Not great.

First, you’ll want to `import React from 'react'` at the top of the file if you weren’t doing so already.

If you’re in VSCode and hover over any underlined element, you’ll get the message “Cannot use JSX unless the ‘ — jsx’ flag is provided.” At this point, you can either click the “Quick Fix” option, or you can fix it manually. If you click “Quick Fix,” you’ll get an option that says “Enable the ‘ — jsx’ flag in your configuration file.” Once you click on it, it takes a second or two to load, and then the errors should go away.

![image](https://github.com/2211rohit/react-with-typescript/assets/53754318/d5259892-64e9-4943-a392-84bbf203eb6b)

Screenshot of a message from VSCode on hovering on a div in `App.tsx`. Highlighted is the option to click quick fix and have VSCode solve it for you.

If you want to do it manually, go into your `tsconfig.json` file, locate the key of `"jsx"`, and change the value to `"react"` instead of `react-jsx`.

If you’re still getting an error in your `tsconfig.js` file, you might be using different versions of TypeScript. Type `cmd + shift + p` to open quick settings in VSCode, and look for `“TypeScript: Select TypeScript version…”`. Click that, and choose `“Use Workspace Version.”`

Hopefully now you are free of any errors, your code is compiling, and you’re ready to get a fantastic app going!
