
# This Project is: Electronic rosary (for muslims)

## Commands Used

run app
```
npm run start
```

build app
```
npm run build
```

## Tools used
- Webpack
- PugJs
- CSS
- SASS
- JS

## How Make it

to install the package
```
npm init
```

to install the webpack bundle to control every thing in this app
```
npm install --save-dev webpack-cli
```

to make the webpack handle the html index
add these lines to: {webpack.config.js} to make it able to work as development server
devServer: {
     ...,
     port: 3000
}
...
plugins: [
    new HtmlWebpackPlugin({
      template: path.join(__dirname, 'src/templates/pages/index.pug'),
      filename: 'index.html'
    })
```
npm i --save-dev html-webpack-plugin
```

to install sass and all dependencies need
```
npm install css-loader sass-loader sass webpack --save-dev
```

add pug plugin
With 'pug-plugin' you can insert your Images, Styles, Fonts & Scripts inside any pug file. Just use "require()" in front of href or src path:
```
npm install pug-plugin --save-dev
```


4- To make it all work, create a "webpack.config.js" file on the root of your project, & add the following settings on it:


📚 Last but not less important:
    You can customize your webpack.config.js and delete or insert anything you like. The code up here it's based on the pug-plugin instructions.

----------------

### then make these things to continue make it work
[how to configure webpack from scratch for a basic website](https://dev.to/antonmelnyk/how-to-configure-webpack-from-scratch-for-a-basic-website-46a5)

To run Webpack, we have to use npm script with simple command webpack and our configuration file as config option. Our package.json should look like this for now:
"scripts": {
    "build": "webpack --config webpack.config.js"
  },


With that basic setup, you can run $ npm run build command. Webpack will look up our entry file, resolve all import module dependencies inside it and bundle it into single .js file in dist folder. In the console, you should see something like this:
```
npm run build
```