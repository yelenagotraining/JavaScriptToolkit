### Repo
[https://github.com/yelenagotraining/JavaScriptToolkit.git](https://github.com/yelenagotraining/JavaScriptToolkit.git)

- Add .editorconfig
- Install editorconfig plugin
- Open command line
  - install node
  - install npm
  - configure global package.json with 
  - goto: https://gist.github.com/coryhouse/9bdb4b1f06695e913ce6f8a722d4d9fd to copy package.json contents
  - create package.json file at the root of your folder and paste the contnets
- install packages by typing `npm install`
- add a folder for scripts
  - In this example its buildScripts folder
- Inside the folder add a script that starts the application 
  - in this projects it's buildScripts/srcServer.js
  - make sure srcServer.js has the app.listen() with a port number
- At a root of a project, add a src or any other main folder and add index.html to server when application is served.
### Sharing Work in progress
- localtunnel
  - npm install localtunnel -g
  - lt --port 3000 (port number specified in your server script)

### Pre/Post Hooks
- in the package.json

### Transpiling with babel

### ESlint

- Create .eslint in the root of your project
- copy an paste contents of http://bit.ly/jsdeveslint into your file
- update your package.json with `   "lint": "esw webpack.config.* src buildScripts --color"`
- to check run: `npm run lint`
- to run lint watch, add following line to package.json script section: `"lint:watch": "npm run lint -- --watch"`
- in command line run with `npm run lint:watch`
- to lint every time you run update your package.json script section with:
 ```json
   "start": "npm-run-all --parallel open:src lint:watch",
   "open:src":"babel-node buildScripts/srcServer.js",
```
### Unit Testing Decisions
1. Framework
   1. Jasmine has it's own assertions
   2. Mocha is more configurable
   3. Jest is for facebook, is a wrapper over Jasmine
2. Assertion Library
   1. Chai
3. Helper Libraries
   1. Cheerio
4. Where to run tests
5. Where to place tests
6. When to run your tests



