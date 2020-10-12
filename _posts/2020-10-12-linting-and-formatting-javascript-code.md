---
layout: post
title: Linting and Formatting JavaScript Code
---

Writing error free code and easy to understand is a must in these days. This can be achieved by adhering to a code style. The most popular code style for JavaScript are [Google JavaScript Style](https://google.github.io/styleguide/jsguide.html), [Airbnb JavaScript Style](https://airbnb.io/javascript/) and [JavaScript Standard Style](https://standardjs.com/).

A tool that can help us writing better code is [ESLint](https://eslint.org/). ESLint will help us identifying problems in our code and it can also enforce us to write code with a code style we choose to adhere. Note that ESLint will only identify and fix small problems like removing semicolons, add missing space before parentheses or so.
If we want to format our code, we can use tool like [Prettier](https://prettier.io/) to automatically format our codes. A formatter is able to format our code, but it is unable to identifyng problems in our code like unused variables, assigning a constant, missing closing bracket, etc.

This is why we need both of them and I will show you how to lint and format JavaScript codes. We will use ESLint to lint our codes with JavaScript Standard Style and `prettier-standard`

### Getting started

First of all we need to create a `package.json` file using `npm init -y` command. This will help us populate `package.json` file easily.

![terminal running npm init command](2020-10-12-linting-and-formatting-javascript-code--01.png)

### Detect problems using ESLint

Then, install ESLint with JavaScript Standard Style configuration by running `npx eslint --init`. This will give you interactive command line and you can use up and down key to navigate, space to select and enter or return to confirm your selection.

![terminal running npx eslint command to choose how to use eslint](2020-10-12-linting-and-formatting-javascript-code--02.png)
![terminal running npx eslint command to choose type of module](2020-10-12-linting-and-formatting-javascript-code--03.png)
![terminal running npx eslint command to choose framework we use](2020-10-12-linting-and-formatting-javascript-code--04.png)
![terminal running npx eslint command to choose whether we use typescript](2020-10-12-linting-and-formatting-javascript-code--05.png)
![terminal running npx eslint command to choose where our code run](2020-10-12-linting-and-formatting-javascript-code--06.png)
![terminal running npx eslint command to choose how to choose code style](2020-10-12-linting-and-formatting-javascript-code--07.png)
![terminal running npx eslint command to choose code style](2020-10-12-linting-and-formatting-javascript-code--08.png)
![terminal running npx eslint command to choose format to save configurations](2020-10-12-linting-and-formatting-javascript-code--09.png)
![terminal running npx eslint command to choose when to install dependencies](2020-10-12-linting-and-formatting-javascript-code--10.png)
![terminal running npx eslint command result](2020-10-12-linting-and-formatting-javascript-code--11.png)

Next, we will install ESLint plugin in our code editor. In my case, I'm using [Sublime Text](https://www.sublimetext.com) and I will use [LSP](https://packagecontrol.io/packages/LSP) and [lsp-eslint](https://packagecontrol.io/packages/LSP-eslint) packages.

Now, create `index.js` file and use code below for testing.

```
[1, 2, 3].map((x) => {
    const y = x + 1;
    return x * y;
});

```

You will see errors like picture below as soon as you paste those code.

![code editor showing errors](2020-10-12-linting-and-formatting-javascript-code--12.png)

This is the benefit of using ESLint to lint our code. ESLint will show the warning and description of the error so we can fix them or ESLint will fix some error when you save the file.

### Beautify code using prettier-standard

ESLint will fix some error like removing trailing semicolon, but it will not format our code. You can try by replacing the code in `index.js` with this code.

```
theFunction(aFunctionName(), codeEatSleepRepeat(), whateverTheElseDoing(), stopBullying(), stopBullying(), stopBullying(), stopBullying());
```

When you save the file, ESLint will only remove the trailing semicolon.

Now, if we want to make our code more readable, we will use `prettier-standard` to format our code. Run `npm install --save-dev prettier-standard` to install it.
Then, we register a command in `package.json` to format our code.

```
{
	...
	"scripts": {
		...
		"lint": "prettier-standard --lint '**/*.{js}'"
	},
	...
}
```

![register command to format code in package.json](2020-10-12-linting-and-formatting-javascript-code--13.png)

Try to run `npm run lint` and you will see your code is automatically formatted and any errors will be displayed in terminal and in the editor.

![errors displayed in terminal](2020-10-12-linting-and-formatting-javascript-code--14.png)
![formatted code](2020-10-12-linting-and-formatting-javascript-code--15.png)

### Why not install formatter in code editor?

First, in my case, it makes Sublime Text freezing when formatting is in process. Using command line to format code is much faster.
Second, you can hook with `precommit` to automatically format your code before committing changes. See [prettier-standard documentation](https://github.com/sheerun/prettier-standard#examples) to do this.

