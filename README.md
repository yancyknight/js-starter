# js-starter
A starter web app. This project was built with the help of Cory House's Pluralsight course Building a JavaScript Development Environment found <a href="https://app.pluralsight.com/library/courses/javascript-development-environment/table-of-contents">here</a>.


## Decisions, decisions
I had to make a lot of decisions while putting this project together. These are the decisions I made and a little bit of reasoning to go with them.

### Editor
I am using Visual Studio Code for this project. I am not including any kind of editor config file because I don't think anyone else will be writing very much code for this project. If this changes, an option is adding a .editorconfig file and using editorconfig.org to sync these preferences between editors.

### Package Manager
I am using NPM as my main package manager, because it's awesome. Also because, if I'm not mistaken, webpack works only with NPM and not Bower, and because Bower is unnecessary.

### Web Server
For development and production I will be using an Express server. I like the consistency of using the same server for development and production.

### Task Automation
I use NPM scripts for task automation. I think Grunt and Gulp are unnecessary abstractions that just add complexity.

### Transpiling
I will be using Typescript as my transpiled language. Since I am planning on using Angular, I would like the greater support from the community and the docs with examples given in Typescript. I also like the intellisense bonuses I get with it out of the box.

### Bundling

### Linting

### Testing and CI

### HTTP

### Project Structure

### Production Build

### Production Deploy