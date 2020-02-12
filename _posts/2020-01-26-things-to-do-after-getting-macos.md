---
layout: post
title: Things to do after getting macOS
---

A new year is started and you might get a new Mac for your new year present. Or, maybe you want to reinstall your Mac because many applications installed and you feel that your OS is *dirty* so you want to clean them up and start *fresh*.
Whatever your reason, here are the things I do to get ready to develop applications in macOS from fresh install you might want to try.

### Update macOS

My MacBook Pro 13" 2017 comes with macOS High Sierra and I want to update or upgrade to the latest macOS available before installing any applications. I think this is important because some applications maybe not supported in the latest macOS.

### Install Fira Code fonts

![fira code samples in various color theme](/assets/images/fira-code-banner.svg)

Fonts with ligatures is perfect for code and I'm falling in love with [Fira Code fonts](https://github.com/tonsky/FiraCode).

### Install Homebrew

![homebrew logo and description](/assets/images/homebrew-social-card.png)

I use Homebrew to install some tools needed for developing applications because installing them individually by downloading from its website then install it to my Mac is troublesome. Using Homebrew, installing a tool is just a command line away.

Try `brew install package_name` to install a package.

#### Tools installed using Homebrew

##### git-flow command

`git-flow` is a tool to help working with GitFlow workflow. Visit `git-flow` [GitHub page](https://github.com/nvie/gitflow) for more information.

##### Node.js

This is an essential tool to develop web applications these days.

##### Other tools

- OpenJDK 8: I use [AdoptOpenJDK](https://github.com/AdoptOpenJDK/homebrew-openjdk) to build Android applications using Cordova.
- Gradle: This one also needed to build Android applications using Cordova.

### Install packages via NPM

These are essential packages to support my development workflow.

- [JavaScript Standard Style](https://standardjs.com): a style checker and linter for JavaScript. I adhere to this coding style in my projects.
- [standard-version](https://github.com/conventional-changelog/standard-version): A changelog generator. This package adhere to [Conventional Commits](https://conventionalcommits.org) and uses [`conventionalcommits preset`](https://github.com/conventional-changelog/conventional-changelog-config-spec).
- [Cordova](https://cordova.apache.org/): a tool to build mobile application using web technologies (HTML, CSS, JS).

### Install Oh My Zsh

![terminal with oh-my-zsh node theme](/assets/images/terminal-with-oh-my-zsh-node-theme.png)

Since macOS Catalina, the default shell for Terminal app is Zsh. And by installing [Oh My Zsh](https://ohmyz.sh), I can improve usability and appearance of the Terminal app because it has many great plugins and amazing themes to suit my desktop theme.

Oh-My-Zsh + [Node theme](https://github.com/skuridin/oh-my-zsh-node-theme) + Fira Code = Terminal above

### Install Sublime Text

Its simplicity and performance makes [Sublime Text](https://sublimetext.com) my favorite text editor.

Sublime Text + Fira Code + Monokai Pro + [some settings](https://gist.github.com/lzaaldian/8fda456f7683a70cc01aa1929276773b) = 🧑🏻‍💻

#### Install Sublime Text Packages

These are the packages/plugins that make Sublime Text awesome for developing web applications.

- [Babel](https://packagecontrol.io/packages/Babel): JavaScript compiler. A must have to build modern web application
- [DocBlockr](https://packagecontrol.io/packages/DocBlockr): multiline comments and function documentation made easy. I use [this settings](https://gist.github.com/lzaaldian/d33e6e0934dd1abeaefca98b698a7875) for generating function documentation.
- [EditorConfig](https://packagecontrol.io/packages/EditorConfig): general coding style configuration for various text editor or IDE.
- [Less syntax highlighting](https://packagecontrol.io/packages/LESS)
- [Sass syntax highlighting](https://packagecontrol.io/packages/Sass)
- [SublimeLinter](https://packagecontrol.io/packages/SublimeLinter): code linter bootstrap. We need to install the linter separately.
  - [SublimeLinter-contrib-standard](https://packagecontrol.io/packages/SublimeLinter-contrib-standard): JavaScript linter using JavaScript Standard Style.
  - [StandardFormat](https://packagecontrol.io/packages/StandardFormat): code formatter for JavaScript Standard Style.
  - [StandardSnippets](https://packagecontrol.io/packages/StandardSnippets): if using Babel as a default JavaScript syntax, the snippets from Sublime Text won't work. This package make it works again with JavaScript Standard Style.
- [Theme - Monokai Pro](https://packagecontrol.io/packages/Theme%20-%20Monokai%20Pro): a perfect theme for Sublime Text.

### Install Sublime Merge

A companion application to Sublime Text. [Sublime Merge](https://sublimemerge.com) is a Git client which well integrated with Sublime Text but also great as a standalone app.

### Install Google Chrome

I use Google Chrome to debug Cordova application installed on Android device. And to test how the application looks like in Android device.

### Install Insomnia

![insomnia application screenshot](/assets/images/insomnia-rest-client.png)

[Insomnia](https://insomnia.rest) is a REST client for testing APIs. It has support for Dark Mode on macOS and have many great themes.

### Install Flow

![flow timer app in macOS](/assets/images/flow-timer-app.png)

[Flow](https://yugen.design/flow/) is a timer application for macOS which adhere to Pomodoro technique. This is a handy app to stay focused and help to get things done.

With your new Mac or refreshed Mac loaded with awesome tools, I hope you can enjoy developing great applications. Have fun and happy coding!.
