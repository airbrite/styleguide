# Tools

Here are some recommended coding tools for Mac...

## Xcode

Make sure Xcode is installed from the App Store

## JDK

Install

```
http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
```

## Homebrew

Install

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor
brew update
```

Recommended Packages

```
brew install wget
brew install git
brew install python
brew install mongodb
brew install phantomjs
brew install lynx
```

## Node

### nvm

Install

```
https://github.com/creationix/nvm
```

Configure

```
nvm install stable
nvm alias default stable
nvm use default
```

### npm

Recommended packages

- nodemon
- grunt-cli
- bower

## Sublime Text 3

Recommended text editor at Celery

```
http://www.sublimetext.com/3
```

### Package Control

```
https://packagecontrol.io/installation
```

### Required Packages

- TrailingSpaces
- JsFormat
- SublimeLinter
- SublimeLinter-jshint
- SublimeLinter-jsxhint
- GitGutter
- LESS
- Handlebars

### Recommended Packages

- DocBlockr
- Babel
- Markdown

### JSHint

[JSHint](https://github.com/jshint/jshint/) is a static code analysis tool that prevents errors and helps to share the same coding style.

You will find a file `.jshintrc` that contains the lint rules per project.

### JsFormat

Uses [js-beautify](https://github.com/einars/js-beautify#options) options.
Will reformat and reindent javascript so that we can share the same coding style.

To configure `JsFormat`:

Goto `Submlime Text -> Preferences -> Package Settings -> JsFormat -> Settings - User` and paste this:

```js
{
  "indent_size": 2,
  "format_on_save": true,
  "jsbeautifyrc_files": true
}
```

## Github for Mac

```
https://mac.github.com/
```
