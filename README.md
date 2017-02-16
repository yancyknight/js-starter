# js-starter
A starter web app. This project was built with the help of Cory House's Pluralsight course Building a JavaScript Development Environment found <a href="https://app.pluralsight.com/library/courses/javascript-development-environment/table-of-contents">here</a>.


## Decisions, decisions
I had to make a lot of decisions while putting this project together. These are the decisions I made and a little bit of reasoning to go with them.

### Editor
I am using <a href="https://code.visualstudio.com/">Visual Studio Code</a> for this project. I am not including any kind of editor config file because I don't think anyone else will be writing very much code for this project. If this changes, an option is adding a .editorconfig file and using <a href="editorconfig.org">editorconfig.org</a> to sync these preferences between editors.

### Package Manager
I am using <a href="https://www.npmjs.com/">NPM</a> as my main package manager, because it's awesome. Also because, if I'm not mistaken, Webpack works only with NPM and not Bower, and because Bower is unnecessary. I may be wrong though.

### Web Server
For development and production I will be using an <a href="http://expressjs.com/">Express</a> server. I like the consistency of using the same server for development and production.

### Task Automation
I use NPM scripts for task automation. I think <a href="http://gruntjs.com/">Grunt</a> and <a href="gulpjs.com/">Gulp</a> are unnecessary abstractions that just add complexity.

### Transpiling
I will be using <a href="https://www.typescriptlang.org/">Typescript</a> as my transpiled language. Since I am planning on using <a href="https://angular.io/">Angular</a>, I would like the greater support from the community and the docs with examples given in Typescript. I also like the intellisense bonuses I get with it out of the box.

### Bundling
<a href="https://webpack.github.io/">Webpack</a> is my bundler of choice. It seems to be the way of the future, with the only other clear competitor right now being <a href="browserify.org/">Browserify</a>, which seems like the bundler of yesterday.

### Linting
<a href="https://palantir.github.io/tslint/">TSLint</a> is the linter I chose. There wasn't a ton of reasoning on this one other than the fact that I'm using Typescript and this seems to be the defacto standard for Typescript linting.

### Testing
I am using <a href="https://mochajs.org/">Mocha</a> and <a href="http://chaijs.com/">Chai</a> to write tests. I am currently debating between <a href="https://github.com/tmpvar/jsdom">JSDom</a> and <a href="https://karma-runner.github.io/1.0/index.html">Karma</a> as my testing frameworks. I need to do more research into Karma.

### Continuous Integration
For this project, I will use <a href="https://travis-ci.org/">Travis CI</a>. For future projects, I may use <a href="https://www.appveyor.com/">AppVeyor</a> because it supports <a href="https://bitbucket.org/">Bitbucket</a>.

### HTTP and API Mocking
This is low on the priority list, but it could be cool to integrate with <a href="https://github.com/json-schema-faker/json-schema-faker">JSON Schema Faker</a> and <a href="https://github.com/typicode/json-server">JSON Server</a>.

### Front End Framework
<a href="https://angular.io/">Angular</a>.

### Project Structure
If I am going to split the app into front end and backend, I think it would be good to separate them in to a client/ and a server/ directory, and then inside each of those separate code by feature.

### Production Build
Kinda overwhelming. Rewatch this module when everything is ready for production.

### Production Deploy
In the Pluralsight course, Cory recommends hosting the front end and the back end separately. I will have to look more into that, but I think it's a great idea. It seems like it's possible to host my front end on <a href="https://www.npmjs.com/package/surge">Surge</a> and my backend on <a href="https://www.heroku.com/">Heroku</a>. Then I can configure my DNS (on <a href="https://domains.google.com">Google Domains</a> or wherever I buy my domain) to point my-domain.com/api/ to the Heroku server and to point my-domain/ to Surge. This would remove the necessity of using <a href="https://github.com/expressjs/cors">CORS</a>.

## TODO
* Configure Webpack
* Configure Express to use Webpack
  * app.use(require('webpack-dev-middleware'))
* Research Karma, decide between Karma and JSDom
* Configure Webpack for production