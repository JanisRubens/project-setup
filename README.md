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
Run `touch babel.config.js`  

Add babel support for webpack/node/typescript.

### Add eslint support
ESlint helps keeping code tidy and consistent.  

Run `npm install eslint --save-dev`  
Run `./node_modules/.bin/eslint --init` this will create `eslintrc` file  
Run `./node_modules/.bin/eslint yourfile.js` to run lint. Create a script that lints all `/src` folder.
Setup your ESlint config in `eslintrc` file  

More about ESlint [Here](https://eslint.org/docs/user-guide/getting-started)
### Add docker support

## Front-end dependencies
### Add webpack support
### Add typescript support

## Back-end dependencies
### Nodemon support.
Nodemon reloads your server on code changes.

Run `npm install nodemon --save-dev`  
Use as `nodemon <back-end entry>.js`  

