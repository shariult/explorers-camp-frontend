## About
Explorer's camp is a personal original project by [Md.Shariul Islam Tuhin](http://shariul.com) . This is frontend of that project. For fullstack project go [here](https://shariul.com/explorers_camp) .
This project is build on SASS, uses 7-1 folder architecture and BEM methodology. Layout is done by using CSS Flexbox. This website is responsive supporting devices with variety of screen sizes.

## Installation
1. Please Install **Node** first, **npm** should automatically be installed. They are required.

2. Run `npm init` to initialize npm directory. Then add following code to package.json:
   `
   "scripts": {
   "watch:sass": "node-sass scss/main.scss css/style.min.css -w",
   "devserver": "live-server",
   "start": "npm-run-all --parallel watch:sass devserver",
   "compile:sass": "node-sass scss/main.scss css/style.compile.css",
   "concat:css": "concat -o css/style.concat.css css/linea.css css/style.compile.css",
   "prefix:css": "postcss --use autoprefixer -b \"last 20 versions\" css/style.concat.css -o css/style.prefix.css",
   "compress:css": "node-sass css/style.prefix.css css/style.min.css --output-style compressed --source-map true",
   "build": "npm-run-all compile:sass concat:css prefix:css compress:css"
   }
   `
3. Some **npm** packages are required for this project, install them by running following command in the terminal,
   `npm i -D live-server node-sass autoprefixer concat postcss-cli npm-run-all`

## For Development run:

`npm start`

## For Production run:

`npm run build`
