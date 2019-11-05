# eslint-template
A simple project template enabling Javascript and Typescript linting and autoformatting via [ESLint](https://eslint.org), [Prettier](https://prettier.io), and [EditorConfig](https://editorconfig.org), with optional presets for [VSCode](https://code.visualstudio.com).

## Usage
The dependencies can be installed via a standard `npm install`.

Two script entries are provided, and can be used as follows:
- `npm test` will run the linter on the project directory and display a report
- `npm run fix` will run the linter on the project directory and auto-fix any auto-fixable issues

## Configuration
Sample **ESLint** ([docs](https://eslint.org/docs/rules/)) and **Prettier** ([docs](https://prettier.io/docs/en/options.html)) configurations are provided in `package.json`; **EditorConfig** ([docs](https://github.com/editorconfig/editorconfig/wiki/EditorConfig-Properties)) requires its own `.editorconfig` file (also provided).

The included settings can (of course) be modified or extended as needed for your particular use case.

For settings that can be configured by both Prettier and EditorConfig (such as `useTabs`/`indent_style`, `endOfLine`/`end_of_line`, etc.), the Prettier setting, if provided, takes precedence. If an ESLint rule also applies (for example, `indent`), it will take precedence over both the others.

The only noteworthy exception is when using tabs for indentation -- EditorConfig's `indent_size` will set the display tab width in Visual Studio Code, but Prettier's corresponding `tabWidth` will not (it only applies when using spaces for indentation).

## Visual Studio Code
If you open the project directory as a folder in VSCode, the provided `.vscode/settings.json` and `.vscode/extensions.json` files will be automatically recognized, and VSCode will prompt you to install the relevant extensions if necessary.

Any linting errors will then appear inline in the code, and a list of all linting errors in any open files can be seen by opening a **Terminal** panel and selecting the **Problems** tab.

Any auto-fixable problems can be auto-fixed by running the standard VSCode **Format Document** command (see the right-click menu); you may need to select `Prettier` as the default formatter to use if prompted. If you enable `editor.formatOnSave` ([docs](https://code.visualstudio.com/docs/getstarted/settings)), then any auto-fixable problems will be auto-fixed every time you save.

(If you haven't run `npm install` before opening the folder in VSCode, linting may not work properly until you've done so and have closed and reopened the VSCode workspace window.)

## License
```
MIT License

Copyright (c) 2019 Brook McEachern

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
