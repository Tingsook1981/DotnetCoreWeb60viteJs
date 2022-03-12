# Vite.js ASP.net Core 6.0 integration

## Start the dotnet app

NPM install as well as JS, SASS and purgeCss compilation are triggered when the the ASP.net solution is built.  

### Building from terminal

`dotnet watch`  

 or 

`CTRL-F5 or F5` 

## Vite package.json

### Install the packages

`npm install`

### Scripts includes in package.json

`npm run dev`
`npm run build`
`npm run preview`
`npm run purgecss`
`npm run watch`

##Vite.js doc
https://vitejs.dev/

##PurgeCSS 

Config with Bootstrap 5 whitelisting dynamic css classes.

`
/* global module */
/* eslint no-undef: "error" */
module.exports = {
    content: [`Views/**/*.cshtml`],
    css: ['wwwroot/app/index.css'],
    // Add css classes used from javascript to ignore purgecss :
    safelist: [
      'carousel-item-start', 
      'carousel-item-end', 
      'carousel-item-next', 
      'carousel-item-prev', 
      'collapsing',
      'show',
      'fade',
      'collapse',
      'collapsed',
      'collapse-horizontal',
      'dropdown-menu',
      'modal-open',
      'fade',
      'show',
      'modal-static',
    ],
    output: 'wwwroot/app/index.css',
    keyframes: true,
    rejected: true,
    variables: true
  }
`


## Credits

Thanks to swildermuth for his explanation on this great Youtube video

https://www.youtube.com/watch?v=L23bAMdgOZA
