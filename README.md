PROJECT STARTER BOILERPLATE

1- npm init    -> INITIALISING THE PROJECT
2- project structure:
new-project
  index.html
  src
    icons
    images
    js
    scss
  node_modules
  package.json
3- npm install node-sass --save-dev		-> installs sass as dev dependency
4- touch .gitignore && echo "node_modules" >> .gitignore	->creates gitignore file and includes node_modules in it
5- "scripts": {
  "scss": "node-sass --output-style compressed -o dist/css src/scss",
}									->compiles scss to css
6- "scripts": {
	"scss": "node-sass --output-style compressed -o dist/css src/scss",
	"serve": "browser-sync start --server --files 'dist/css/*.css, **/*.html'"	->reloads page when files change
}
7- "scripts": {
	"scss": "node-sass --output-style compressed -o dist/css src/scss",
	"serve": "browser-sync start --server --files 'dist/css/*.css, **/*.html'",
	"watch:css": "onchange 'src/scss' -- npm run scss",
}											->watches changes using the onchange package and runs scss 												  script when changes occur
8-   "start": "npm run serve && npm run scss"			->runs both scripts
9-   npm install npm-run-all --save-dev				->run commands in parallel
     "start": "run-p serve watch:css"



