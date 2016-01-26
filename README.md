# Node to Cloud

# Stage 0 - Hello World

This stage introduces you to Node, get your feet wet with a simple Hello World script. 

First, a little background. Node JS is an increasingly popular technology, especially in startup land. 
Node is popular for a number of reasons. 

1. Write in the same language on the front and back-end. 
2. Modules are increasingly being shared between the front and back-end, making the ecosystem grow very large. 
3. Does very well cross-platform. Write on Mac, Linux, or Windows and enjoy a good experience. 
4. The architecture is event-driven and asynchronous, providing performance and scaling advantages. Many developers prefer this architecture to a multi-threaded environment, which has been known to be perilous. 
5. Javascript is the client language for more and more database technologies, thus, again, you gain the language advantage. 

There are many other advantages of Node. I prefer the tech stack for the ease and speed of getting an application going. 

This demo will focus on getting us started with Node and getting our application to production fast. We won't spend a ton of time writing code - I'll let you dream up what type of application you want to build. 
We're going to spend most of the time today getting the scaffolding of our project going and getting the deployment architecture in place. 

**Tooling**

Install all the needed tools. 

1. Node - `brew update &&  brew install node` (alternatively install via [nodejs](https://nodejs.org/en/download/))).
2. VS Code - install on [VS Code's website](https://code.visualstudio.com/) and [CL tool](https://code.visualstudio.com/docs/editor/setup).

    Linux

    `sudo ln -s /path/to/vscode/Code /usr/local/bin/code`

    Mac

    `echo "function code () { VSCODE_CWD="$PWD" open -n -b \"com.microsoft.VSCode\" --args $*; }" >> .zshrc`

**Hello World**

Navigate to the location of your projecdt. 

```zsh
cd ~/<my-project>
```

Create a node project. This command will guide you through creating a `package.json` file. Don't worry about too much here (you can see more [here](https://docs.npmjs.com/files/package.json)), other than specifying that the entry point is `server.js`. 

```zsh
npm init
```

Create a new server file. 

```zsh
touch server.js
```

Install project specific dependencies. 

```zsh
npm install express --save
```

If you look now, you will see a new directory called `node_modules`. Run `ls` on that directory and you'll see express installed a number of dependencies. Additionally, you'll see `express` in your list of dependencies in your `package.json` file. 

Write the following code in that file. 

```node
var express = require('express');
var app = express();

app.get('/', function(req, res) {
   res.send('Hello World'); 
});

app.listen(3000, function() {
   console.log('Example app listening on port 3000!'); 
});
```
    
Run the code.

```zsh
node server.js
```

Navigate to `localhost:3000` in your browser.

Congratulations! You are running a Node server. 

## Resources

* [Node Docs](https://nodejs.org/api/)
* [Express JS Hello World Example](http://expressjs.com/en/starter/hello-world.html)
* [NPM Package.json Docs](https://docs.npmjs.com/files/package.json)
