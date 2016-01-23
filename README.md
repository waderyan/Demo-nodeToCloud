# Node to Cloud

# Stage 2 - VS Code Features

The text editor you use matters at this stage (in all other stages it doesn't). This stage will demo some of the useful
features VS Code has for writing and debugging a Node application. 

**Intellisense**

Intellisense is a dev editor tool for coding productivity. Intellisense is an IDE feature that gives context-aware suggestions while writing code. 

Install TSD. TSD stands for TypeScript Definition Manager makes it easy to install TypeScript definition files into your workspace. 
TypeScript definition files are what powers intellisense. 

```zsh
$ npm install -g tsd
```

Pull down the Node and Express definition files. 

```zsh
$ tsd query node express --action install
```

Look at the root of your project. There is a new directory called typings. Within that directory are TSD files (`*.d.ts`). VS Code uses 
those definition files to provide intellisense. 

For example, let's go to app.js (remember this is the starting point of our Node application). 

On the last line of app.js start typing `console.`. Intellisense will show you what methods you can call. This brings the API docs to your finger tips
as you type. 

**Extensions**

Extensions allow you to customize your code editing experience. There are hundreds of extensions and more and more coming everyday. 

Type `cmd+shift+p` to open the command promp within VS Code. Now type "Install Extensions". You will see a list of extensions you can install. 
You can browse for extensions here or in the [marketplace](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&cad=rja&uact=8&ved=0ahUKEwiy5tX4k7TKAhVEzGMKHRoQDqkQFggcMAA&url=https%3A%2F%2Fmarketplace.visualstudio.com%2F&usg=AFQjCNEjSwCtmqzyky5NS2teOa4IN5uSRQ&sig2=hdrxaQkz1eENVUyOIkqRBw&bvm=bv.112064104,d.cGc). 

Some extensions I find useful. 

* [Spelling and Grammar](https://marketplace.visualstudio.com/items/seanmcbreen.Spell)
* [Add jsdoc comments](https://marketplace.visualstudio.com/items/stevencl.addDocComments)
* [jshint](https://marketplace.visualstudio.com/items/dbaeumer.jshint)
* [Chrome Debugger](https://marketplace.visualstudio.com/items/msjsdiag.debugger-for-chrome)
* [Bookmarks](https://marketplace.visualstudio.com/items/alefragnani.Bookmarks)

**Debugging**

One of the strongest features of VS Code is the debugging functionality. When I was learning Node the biggest frustration I had was a lack of debugging tools. 

To debug follow these steps. 

1. Click on the debug icon on the far left. 
2. Click the configure icon to create a default `launch.json` file. 
3. Click the green play icon to start the application in debug mode. 
4. Open app.js and place a break-point on the `console.log()` line. 
5. Click the refresh icon. 

This gives the application and easy to configure debugger. 

**Git Integration**

1. Change one of your files. 
2. Click the Git icon to the far left. 
3. See the changes, stage, commit, and push inside VS Code. 

## Resources

* [VS Code Debugging](https://code.visualstudio.com/Docs/editor/debugging)
* [VS Code NodeJS End-to-End](https://code.visualstudio.com/docs/runtimes/nodejs)
* [Definitely Typed Repository](https://github.com/borisyankov/DefinitelyTyped)