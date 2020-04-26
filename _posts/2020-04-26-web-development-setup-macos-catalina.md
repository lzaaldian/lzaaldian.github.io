---
layout: post
title: Web Development Setup on macOS Catalina
---

After spending some time finding the best way to setup my MacBook Pro for developing web applications, finally I can stop for a while and start enjoying what I like - develop web applications. So, here's what I found.

### What's already installed?

For web development, we have these stuff already installed:

- Apache web server
- PHP
- Git

Now, we can start installing the other stuff.

### Install Homebrew

Homebrew is *de-facto* package and application manager for macOS. It really does what it said "Install **the stuff you need** that Apple didn't". I'm surprised that it has many popular applications ready to be installed so we don't have to go to download page and install the apps manually.

Visit [Homebrew website](https://brew.sh) to install and we will go to the next step.

### Install Oh My Zsh

Since macOS Catalina, the default shell for Terminal is `zsh`. But, still lack of style in my opinion. Oh My Zsh will supercharge your Terminal by utilizing powerful plugins and beautiful themes.

Go to [Oh My Zsh website](https://ohmyz.sh) to install and get ready to make Terminal more enjoyable.

### Become a Professional Dracula 🧛🏻‍♂️

It's not about how to get money by sucking bloods like a dracula. But, using [Dracula Pro](https://draculatheme.com/pro) theme in your tools. I use Dracula Pro for my desktop wallpaper, Terminal app and Sublime Text. For other apps, I use regular Dracula theme.

Here's how a professional dracula looks like

screenshot of desktop with dracula themes

### Install Git Flow

I use Git Flow workflow for versioning my code. The tool I use is `git-flow` and it can be installed via Homebrew.

```
brew install git-flow
```

### Install Package Managers

#### Install Node.js

A must have for developing front-end of web application.

```
brew install node
```

#### Install Composer

A must have for developing PHP web application.

```
brew install composer
```

### Install Tools via NPM

#### JavaScript Standard Code Style Linter

[![JavaScript Style Guide](https://cdn.rawgit.com/standard/standard/master/badge.svg)](https://github.com/standard/standard)

I use `standard` in my projects because it's simple, no configuration needed.

```
npm install -g standard
```

#### Standard Version

Automate versioning and CHANGELOG generation, with [Semantic Versioning](https://semver.org) and [Conventional Commits](https://conventionalcommits.org)

```
npm install -g standard-version
```

### Install Applications via Homebrew

#### Victor Mono Fonts

[This unique and awesome font](https://rubjo.github.io/victor-mono/) is like match made in heaven with Dracula theme.

```
brew tap homebrew/cask-fonts
brew cask install font-victor-mono
```

#### Sublime Text and Sublime Merge

Magnificent duo for web development. I have tried another IDE and code editors, but they don't feel good in my opinion. I love Sublime Text performance and simplicity.

```
brew cask install sublime-text sublime-merge
```

#### Google Chrome

Most used browser in the world. I primarily use Safari, but when I need to audit website or web application, I use Google Chrome. Its Lighthouse powered audit tool like [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) can only give complete result if accessed using Chrome based browsers and [web.dev](https://web.dev/measure/) only measure for mobile.

```
brew cask install google-chrome
```

#### Insomnia REST Client

My REST client of choice, because I can use Dracula theme on this app and of course because of its simplicity and ease of use.

```
brew cask install insomnia
```

### Sublime Text Packages

It's time to supercharge Sublime Text for web development. Get these packages installed.

- [AdvancedNewFile](https://packagecontrol.io/packages/AdvancedNewFile): Makes it easier to create new file.
- [Babel](https://packagecontrol.io/packages/Babel): Syntax definitions for ES6 with React JSX extensions.
- [DocBlockr](https://packagecontrol.io/packages/DocBlockr): multiline comments and function documentation made easy. I use [this settings](https://gist.github.com/lzaaldian/d33e6e0934dd1abeaefca98b698a7875) for generating function documentation.
- [EditorConfig](https://packagecontrol.io/packages/EditorConfig): general coding style configuration for various text editor or IDE.
- [Less syntax highlighting](https://packagecontrol.io/packages/LESS)
- [Sass syntax highlighting](https://packagecontrol.io/packages/Sass)
- [SublimeLinter](https://packagecontrol.io/packages/SublimeLinter): code linting framework. We need to install the linter individually.
  - [SublimeLinter-php](https://packagecontrol.io/packages/SublimeLinter-php): Lint PHP using `php -l`.
  - [SublimeLinter-contrib-standard](https://packagecontrol.io/packages/SublimeLinter-contrib-standard): JavaScript linter using JavaScript Standard Style.
  - [StandardFormat](https://packagecontrol.io/packages/StandardFormat): code formatter for JavaScript Standard Style.
  - [StandardSnippets](https://packagecontrol.io/packages/StandardSnippets): if using Babel as a default JavaScript syntax, the snippets from Sublime Text won't work. This package make it works again with JavaScript Standard Style 🤩.

After installing those packages. I recommend to use [this settings](https://gist.github.com/lzaaldian/8fda456f7683a70cc01aa1929276773b) for Sublime Text.

Now, we are ready to code with style 😎
