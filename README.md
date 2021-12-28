# Project-setup
Bunch of instructions so I dont have to google each time I start a project.

### [Optional] Set npm init defaults.
Example:
```
npm config list  
  
npm set init.author.name "<Your Name>"  
npm set init.author.email "you@example.com"  
npm set init.author.url "example.com"  
npm set init.license "MIT"  
```

### Initialize a project with npm.
Run `npm init` this will ask bunch of questions.  
Run `npm init -y` to skip all questions.  
More about the command [Here](https://docs.npmjs.com/cli/v8/commands/npm-init).  

### Initialize .git repo for the project.
Run `git init`  
Add git project files.
`touch .gitignore`
`touch README.md`
`touch CHANGELOG.md`
Run `git add . && git commit -m 'Initial commit'`.  

## Project dependencies
### Add babel support
Babel is a javascript compiler that compiles beta features in vannila js.  
More about babel setup [Here](https://babeljs.io/)
  
Install core dep:  
Run `npm install --save-dev babel-loader @babel/core` 
Create babel config file:  
Run `touch babel.config.js` -- This is for global babel presets  
Run `touch .babelrc` -- This is for file/directory specific presets    

Add babel support for webpack/node/typescript.

### Add eslint support
ESlint helps keeping code tidy and consistent.  

Run `npm install eslint --save-dev`  
Run `./node_modules/.bin/eslint --init` this will create `eslintrc` file  
Run `./node_modules/.bin/eslint yourfile.js` to run lint. Create a script that lints all `/src` folder.  
Setup your ESlint config in `eslintrc` file  
Create `.eslintignore` and add nodemodules to it if you are using global eslint

More about ESlint [Here](https://eslint.org/docs/user-guide/getting-started)  

### Add config file support
There are multiple good config dependencies like .dotenv cross-env and config.  
For time being I choose config.  

Run `npm install config`  
Run `mkdir config`  
Run `touch default.yml`  
Run `touch local.yml`  

More about the dependency [Here](https://www.npmjs.com/package/config)

### Add docker support

## Front-end dependencies
### Add webpack support
Bundler for JS code.  

Install deps:  
Run `npm install --save-dev webpack webpack-dev-server webpack-cli`  
Create config file:  
Run `touch webpack.config.js`  
Really simple webpack config example:  
```
const path = require('path');

module.exports = {
  entry: path.resolve(__dirname, './src/index.js'),
  output: {
    path: path.resolve(__dirname, './dist'),
    filename: 'bundle.js',
  },
  devServer: {
    contentBase: path.resolve(__dirname, './dist'),
  },
};
```
Add script to package.json file:  
`"dev": "webpack serve --config ./webpack.config.js --mode development",`  

Plugins worth adding:  
* [Manifest](https://www.npmjs.com/package/webpack-manifest-plugin) - adds content hashes that helps with browser caching.  
* [Clean WP](https://www.npmjs.com/package/clean-webpack-plugin) - removes/cleans your build folder(s).  
* [Copy WP](https://www.npmjs.com/package/copy-webpack-plugin) - Copies files/directories to build folder.  
* [Html WP](https://www.npmjs.com/package/html-webpack-plugin) - Creates html files with hashes for build folder.  
* 

### Add typescript support

## Back-end dependencies
### Nodemon support.
Nodemon reloads your server on code changes.

Run `npm install nodemon --save-dev`  
Use as `nodemon <back-end entry>.js`  


### Helpful links:
Really nice blog for setting up a lot of modern things. [Here](https://www.robinwieruch.de/javascript-project-setup-tutorial/)

