# Webpack 2 - StartedKit

## Dependency

1. webpack v2
2. webpack devServer
3. react
4. react-dom
5. react-hot-loader
6. babel-cli
7. babel-loader
8. babel-preset-es2015
9. babel-preset-react
10. babel-preset-stage-0
11. babel-plugin-transform-decorators-legacy
12. eslint
13. babel-eslint

## Target

### npm / yarn: package.json

- [x] Build production mode script.
- [ ] Adjust devDependency and Dependency to serve CI-server and Production-server.

### Webpack: webpack.config.bable.js, devServer.js

- [x] Migrate webpack settings from v1 to v2.
- [x] webpack ``` webpack.optimize.UglifyJsPlugin() ``` adjust.
 > 1. using ``` webpack -p ``` command, webpack will auto add ``` webpack.optimize.UglifyJsPlugin() ```. If you add ``` webpack.optimize.UglifyJsPlugin() ``` and using ``` webpack -p ``` at the same time, you will get error message when you are building app.
 > 2. If you want to ``` webpack.optimize.UglifyJsPlugin() ``` and ``` webpack -p ``` at the same time, you need to remove ``` config.devtool ``` option.
 - [x] webpack entry setting.

### Babel: .babelrc

- [x] New version babel setting adjust.(Need not do anything.)

### Eslint: .eslintrc, package.json

- [x] Add eslint settings and script.
- [x] Add .eslintignore to ignore specific files and directories.
- [x] Eslint run check script for auto check.

### React

- [x] React-hot-loader setting adjust.(put it on top of entry.)

### CI server(prepare script)

- [x] run ``` npm install --only=dev ``` to install only devDependency in package.json.
- [x] run ``` npm run eslint ``` to check coding rule.
- [x] run ``` npm run build:prod ``` to bundle JavaScript for production mode.
- [ ] run build script to devide enviroment to handle api url.

### Production server(prepare script)

- [ ] run only ``` npm run serve ``` to host index.html.