# Settings for `roc-package-web-component-dev`

## Build

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| assets             | An array of files to include into the build process.                                                                      | build.assets              | --build-assets              | `null`                            | `[Filepath]`                                         | No       |
| disableProgressbar | Should the progress bar be disabled for builds.                                                                           | build.disableProgressbar  | --build-disableProgressbar  | `false`                           | `Boolean`                                            | No       |
| libraryTarget      | Which format to export the component as.                                                                                  | build.libraryTarget       | --build-libraryTarget       | `"umd"`                           | `/^var$|^this$|^commonjs$|^commonjs2$|^amd$|^umd$/i` | No       |
| mode               | What mode the application should be built for. Possible values are &quot;dev&quot; and &quot;dist&quot;.                  | build.mode                | --build-mode                | `"dist"`                          | `/^dev|dist$/i`                                      | No       |
| name               | The name of the generated application bundle.                                                                             | build.name                | --build-name                | `null`                            | `String`                                             | Yes      |
| path               | The basepath for the application.                                                                                         | build.path                | --build-path                | `"/"`                             | `Filepath`                                           | No       |
| targets            | For what targets the code should be built for.                                                                            | build.targets             | --build-targets             | `["web","es5","es6"]`             | `[/^web$|^es5$|^es6$/i]`                             | No       |

### Input

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| es5                | What directory to build from.                                                                                             | build.input.es5           | --build-input-es5           | `"src"`                           | `Filepath`                                           | No       |
| es6                | What directory to build from.                                                                                             | build.input.es6           | --build-input-es6           | `"src"`                           | `Filepath`                                           | No       |
| web                | What file to use as entry file.                                                                                           | build.input.web           | --build-input-web           | `"src/index.js"`                  | `Filepath`                                           | No       |

### Output

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| es5                | The output directory for the ES5 build.                                                                                   | build.output.es5          | --build-output-es5          | `"build/es5"`                     | `Filepath`                                           | No       |
| es6                | The output directory for the ES6 build.                                                                                   | build.output.es6          | --build-output-es6          | `"build/es6"`                     | `Filepath`                                           | No       |
| web                | The output directory for the Web build.                                                                                   | build.output.web          | --build-output-web          | `"build/web"`                     | `Filepath`                                           | No       |

### Style
Settings for style related things.

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| autoprefixer       | Settings for Autoprefixer.                                                                                                | build.style.autoprefixer  | --build-style-autoprefixer  | `[{"browsers":"last 2 version"}]` | `[{}]`                                               | No       |
| modules            | If CSS Modules should be enabled.                                                                                         | build.style.modules       | --build-style-modules       | `true`                            | `Boolean`                                            | No       |
| name               | The naming pattern to use for the built style files.                                                                      | build.style.name          | --build-style-name          | `"[name].[hash].css"`             | `Unknown`                                            | No       |

## Dev

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| debug              | Filter for debug messages that should be shown during development, see https://npmjs.com/package/debug.                   | dev.debug                 | --dev-debug                 | `"roc:*"`                         | `String`                                             | No       |
| demoPort           | The port that the demo server starts on.                                                                                  | dev.demoPort              | --dev-demoPort              | `3002`                            | `Integer`                                            | No       |
| port               | Port for the dev server.                                                                                                  | dev.port                  | --dev-port                  | `3001`                            | `Integer`                                            | No       |

### Browsersync
Settings for Browsersync.

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| enabled            | If Browsersync should be enabled.                                                                                         | dev.browsersync.enabled   | --dev-browsersync-enabled   | `true`                            | `Boolean`                                            | No       |
| open               | If Browsersync should open when the server is ready.                                                                      | dev.browsersync.open      | --dev-browsersync-open      | `true`                            | `Boolean`                                            | No       |
| port               | The port that Browsersync should start on, should be a range of at least 2                                                | dev.browsersync.port      | --dev-browsersync-port      | `3030`                            | `Integer`                                            | No       |

### DevMiddleware

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| noInfo             | If no info should be sent to the console.                                                                                 | dev.devMiddleware.noInfo  | --dev-devMiddleware-noInfo  | `true`                            | `Boolean`                                            | No       |
| quiet              | If nothing should be sent to the console.                                                                                 | dev.devMiddleware.quiet   | --dev-devMiddleware-quiet   | `false`                           | `Boolean`                                            | No       |

### HotMiddleware

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| noInfo             | If no info should be sent to the console.                                                                                 | dev.hotMiddleware.noInfo  | --dev-hotMiddleware-noInfo  | `false`                           | `Boolean`                                            | No       |
| overlay            | If a overlay should be shown when an error has occurred.                                                                  | dev.hotMiddleware.overlay | --dev-hotMiddleware-overlay | `false`                           | `Boolean`                                            | No       |
| quiet              | If nothing should be sent to the console.                                                                                 | dev.hotMiddleware.quiet   | --dev-hotMiddleware-quiet   | `false`                           | `Boolean`                                            | No       |
| reload             | If the browser should be reloaded if it fails to hot update the code.                                                     | dev.hotMiddleware.reload  | --dev-hotMiddleware-reload  | `true`                            | `Boolean`                                            | No       |

### Template

| Name               | Description                                                                                                               | Path                      | CLI option                  | Default                           | Type                                                 | Required |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------------------------- | --------------------------------- | ---------------------------------------------------- | -------- |
| name               | The name of the templates. Uses nunjucks and two variables are available, &quot;name&quot; and &quot;bundlePath&quot;.    | dev.template.name         | --dev-template-name         | `"development.html"`              | `String`                                             | No       |
| path               | Path to a directory where the template can be found, can be both relative based on current working directory or absolute. | dev.template.path         | --dev-template-path         | `null`                            | `Filepath`                                           | No       |