# FED Meetup Chapter - April 2020

**Point Covered**
* Setup a project from scratch using CLI and Package Manager

**Tools/Prerequisites for getting started**
* make sure your machine is connected with the Internet :D 
* [Node Js](https://nodejs.org/en/download/) (LTS version recommended)
* basic understanding of [CLI](https://www.w3schools.com/whatis/whatis_cli.asp)
* basic understanding of [package managers](https://blog.idrsolutions.com/2018/07/what-is-a-package-manager-and-why-should-you-use-one/)
    * A package manager is a programming language’s tool to create project environments and easily import external dependencies.
* [NPM](https://www.npmjs.com/)
* basic understanding of [package.json](https://www.digitalocean.com/community/tutorials/nodejs-package-json) file

**Packages used**
* [Jquery](https://www.npmjs.com/package/jquery)
* [Bootstrap](https://www.npmjs.com/package/bootstrap) | [Documentation](https://getbootstrap.com/)
* [Laravel-mix](https://www.npmjs.com/package/laravel-mix) | [Installation Guide](https://laravel-mix.com/docs/5.0/installation)

**Step by step guide to create a project**
* Create a directory/folder and open this in command prompt/terminal (for this you need basic understanding of [CLI](https://www.w3schools.com/whatis/whatis_cli.asp) like how to navigate to particular directory)
* Type below command to generate package.json file (this command only work if your machine has [Node/NPM](https://nodejs.org/en/download/) installed)  
```
npm init -y
```
*  now you can check in your folder for [package.json](https://www.digitalocean.com/community/tutorials/nodejs-package-json) file
* now create SRC directory with necessary files(In this directory we will write our development code)
![src directory](https://user-images.githubusercontent.com/38717853/80941510-4101c280-8e00-11ea-9ad6-bf7d141c02a5.png)
* let's add packages listed at top by following commands
```
npm i jquery
npm i bootstrap
npm i laravel-mix
```
* now include bootstrap to our app.scss file
```
@import "~bootstrap/scss/bootstrap";
```
![add-bootstrap-to-scss](https://user-images.githubusercontent.com/38717853/80942248-f08b6480-8e01-11ea-8117-6354ba4ae160.png)
* now include jquery and bootstrap js to our app.js file
```
require("jquery");
require("bootstrap/dist/js/bootstrap.bundle");
```
![add jquery and bootstrap js to app.js file](https://user-images.githubusercontent.com/38717853/80942549-b078b180-8e02-11ea-8f27-81ffc7578e51.png)
```
require("jquery");
require("bootstrap/dist/js/bootstrap.bundle");
``` 
* now it's time to generate webpack.mix.js file at root level of our directory(for compiling/bundling our scss and js file to our production folder. you can check [laravel-mix](https://laravel-mix.com/docs/5.0/installation) documentation for more)
```
let mix = require('laravel-mix');
mix.js('src/js/app.js', 'public/assets/js/')
   .sass('src/scss/app.scss', 'public/assets/css/');
``` 
![webpack.mix.js](https://user-images.githubusercontent.com/38717853/80942773-46acd780-8e03-11ea-8b39-81c834e72c9b.png)
* now add scripts to our package.json file. scripts can be found [here](https://laravel-mix.com/docs/5.0/installation#npm-scripts) (please read the [package.json](https://www.digitalocean.com/community/tutorials/nodejs-package-json) anatomy if you don't familiar with that)
![](https://user-images.githubusercontent.com/38717853/80943018-d8b4e000-8e03-11ea-8e64-2e9e1c98a20f.png)
* now hit this command for handle different environments(mac and windows)
```
npm install cross-env --save-dev
```
* we are done, now just run following command and see the magic :D
```
npm run watch
```
* now if you check your project directory you should see public folder with your js and css file, so you can use this as you want  
![final folder structure](https://user-images.githubusercontent.com/38717853/80943782-9ab8bb80-8e05-11ea-8158-ddfc772dd7f2.png)

*Please note that all things we discussed/referred is our own way to get work done. this is not recommended/useful in all cases so think about what fits best to you*  

* currently we dont have any social media accounts for this meetup/community so meanwhile you can stay connected with me on [twitter](https://twitter.com/suvagiyajd?lang=en), [LinkedIn](https://in.linkedin.com/in/s-jaydip), and [instagram](https://www.instagram.com/jaydip.suvagiya/) for further updates for upcoming meetups.   
