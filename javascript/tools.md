# Tools

## [JSHint](https://github.com/jshint/jshint/)

[JSHint](https://github.com/jshint/jshint/) is a static code analysis tool that prevents errors and helps to share the same coding style.

You will find a file `.jshintrc` that contains the lint rules per project.

### Sublime Text

Use the `JSHint Gutter` package.

To configure `JSHint Gutter`:

1. Goto `Submlime Text -> Preferences -> Package Settings -> JSHint Gutter -> Set Plugin Options`
2. Set `"link_on_edit": true` and `"lint_on_save": true`.

Many other text editors and IDEs has a JSHint plug-in or you can use it from the
command-line via `jshint <filename>`. If you don't have it installed yet,
just run `npm install -g jshint`.

## JSFormat / [JS Beautifier](https://github.com/einars/js-beautify#options)

[JS Beautifier](https://github.com/einars/js-beautify#options) will reformat and reindent javascript so that we can share the same coding style.

### Sublime Text

Use the `JsFormat` package.

To configure `JsFormat`:

1. goto `Submlime Text -> Preferences -> Package Settings -> JsFormat -> Settings - User` and paste this:

```js
{
  "indent_size": 2,
  "format_on_save": true,
  "jsbeautifyrc_files": true
}
```

Everything else can be left to the default settings.
