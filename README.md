## How To Deploy an Express API on Vercel.
Link:https://fahimahammed-cse.medium.com/deploy-an-express-api-on-vercel-eebc13ace629 (Written by, Fahim Ahammed Firoz vai)

## How to Create an Express API Server??
First, Go to the site https://expressjs.com/en/starter/installing.html
Secondly, According to the documentary, the tasks must be done step by step.

## Details
১. প্রথমে একটা Folder খুলতে হবে।[useing ($ mkdir myapp) on command prompt]
এবং তারপরে cmd তে গিয়ে cd দিয়ে Folder এর ভিতরে যেতে হবে। যেমন: $ cd myapp

২. Use the npm init command to create a package.json file for your application. 
$ npm init -y

৩. Now install Express in the myapp directory and save it in the dependencies list. For example:
$ npm install express

৪. create a index.js file and write the code as below:


    const express = require('express');
    const app = express();
    const port = 5000;

    app.get('/', (req, res) => {
    res.send('Hello World!');
    });

    app.listen(port, () => {
    console.log('Example app listening on port', port);
    });

                                                        
Extra--

i. Update for Live Code_ Please Install nodemon for ever project.

ii. ওয়েবসাইটে Api data ব্যবহার করার জন্য cors install  করতে হবে।
    Go to --- expressjs.com and then > Resources > Middleware > cors

    > cmd Cors Install code --
     $ npm install cors

    And Include the (index.js) file---


    app.use(cors())
                

iii. For deploy purpose, create a (.gitignore) file and write the code as below:

/node_modules/
  

