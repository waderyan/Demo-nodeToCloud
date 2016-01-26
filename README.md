# Node to Cloud

# Stage 1 - Yo

In this stage we scaffold our project. 

Yo is short for Yeoman. Yeoman is a very useful npm package for creating project scaffolding. The web dev world is exploding in popularity. 
Tools like Yeoman help to connect all the different tools together.

The express generator creates a Node Express app scaffolding. There are a huge variety of generators for all types of stacks.

**Tooling**

1. Yo - `$ npm install -g yo`
2. Express Generator - `$ npm install -g generator-express`
3. Sass - `$ gem install sass`  (If Ruby is not installed you'll need to do [that](https://www.ruby-lang.org/en/documentation/installation/) first.)

**Create app scaffolding**

```zsh
yo express
# Would you like to create a new directory for your project? n
# Select a version to install: Basic
# Select a view engine to use: Jade
# Select a css preprocessor to use: Sass
# Select a build tool to use: Gulp
```

Yoeman gives us all sorts of options within the generator. 
We've chosen the above, but you could easily choose different options and end up with a different scaffold. 

Some explanations for the above options. 

* Jade - is a type of view engine. View engines create HTMl files from special files that are a mix of HTML and a programming language. 
This allows you to embed programming logic in an HTML page and have it served up after completing the logic. 
* Sass - is a css preprocessor. It is a programming language for extending CSS. `sass` files go through a pre-processing and are spit out as `css` files.
Similar to what happens with `jade` files. 
* Gulp - is a front end build tool, commonly called a task runner. Gulp will automate your workflow and help manage your other tools.
* Bower - Bower was not specified by Yo, but we use it. Bower manages external dependencies (i.e. other node modules the application depends on).  

**Explore generated files**

Let's take a look at the generated files to get a feel for what we have to work with. 

* `app/` - contains the application code. This is the front end and the backend. 
  
We could talk about MVC all day if we wanted. There is a lot to code design, but the above gives us a 10,000 foot view. 

* `config/` - configuration files for the application. 
* `node_modules/` - directory of node modules used by the application. See package.json for the list. 
* `public/` - all the files that are given (served up) to the client. 
  * `components/` - independent pieces of the UI, commonly called components. 
  * `css/` - stylesheets (post sass compilation). 
  * `img/` - images
  * `js/` - javascript files. 
* `.bowerrc` - configuration for bower. 
* `.editorconfig` - configuration for editors (i.e. VS Code). 
* `.gitignore` - files we want git to ignore. 
* `app.js` - node application code. This is the server's starting point. 
* `bower.json` - bower's manifest file. 
* `gulpfile.js` - code to run and specify gulp tasks. 
* `package.json` - manifest file for the application. 

**Start the application**

Start gulp "default" task. 

```zsh
$ gulp 
```

Navigate to [localhost:3000](http://localhost:3000) to view your application. 

Gulp is running a module that is watching our files for changes. When the module detects a change, gulp will reload our application. 

Try adding text after `#{title}`. Your application will reload for you. 

Additionally, we can add new files. Let's create a new view. 

1. Right click on the `views` folder in VS Code. 
2. Click New File. 
3. Enter "test.jade"
4. Type `p = "I am a test file"` in test.jade
5. Navigate to index.js and add the following route after `router.get('/'...`

```js
router.get('/test', function(req, res) {
  res.render('test');
});
```

Now navigate to [localhost:3000/test](http://localhost:3000/test). 

## Resources

* [Node Docs](https://nodejs.org/api/)
* [Express Docs](http://expressjs.com/en/4x/api.html)
* [Express Generator](https://www.npmjs.com/package/generator-express)
* [Yo](http://yeoman.io/)
* [SO: What is view engine?](http://stackoverflow.com/questions/8308485/what-is-view-engine-what-does-it-actually-do)
* [Jade language reference](http://jade-lang.com/reference/)
* [Sass Docs](http://sass-lang.com/)
* [Gulp Docs](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md)
