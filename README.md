## Customize by Bipul Hossain
### Based on the Doc [How To Deploy an Express API on Vercel.](https://fahimahammed-cse.medium.com/deploy-an-express-api-on-vercel-eebc13ace629)  Written by, [Fahim Ahammed Firoz](https://github.com/fahimahammed) vai 
## How to Create an Express API Server??
* First, Go to the site [expressjs.com](https://expressjs.com/en/starter/installing.html)
* Secondly, According to the documentary, the tasks must be done step by step.

## Details
i. প্রথমে একটা Folder খুলতে হবে।[useing ($ mkdir myapp) on command prompt]
এবং তারপরে cmd তে গিয়ে cd দিয়ে Folder এর ভিতরে যেতে হবে। যেমন:

```ruby
cd myapp

```

ii. Use the npm init command to create a package.json file for your application. 

```ruby
npm init -y
```

iii. Now install Express in the myapp directory and save it in the dependencies list. For example:

```ruby
npm install express
```

iv. create a index.js file and write the code as below:

```ruby
    const express = require('express');
    const app = express();
    const port = 5000;

    app.get('/', (req, res) => {
    res.send('Hello World!');
    });

    app.listen(port, () => {
    console.log('Example app listening on port', port);
    });
    
```
                                                        
Extra:

i. Update for Live Code_ Please Install nodemon for ever project.

```ruby
    npm install -g nodemon
```
    
ii. ওয়েবসাইটে Api data ব্যবহার করার জন্য cors install  করতে হবে।
    Go to [expressjs.com](https://expressjs.com/en/starter/installing.html) and then > Resources > Middleware > cors.
    * cmd Cors Install code:
    
 ```ruby 
    npm install cors
 ```
 
    *And Include the (index.js) file.
    
```ruby 
    const cors = require('cors')
    app.use(cors())
```           

iii. For deploy purpose, create a (.gitignore) file and write the code as below:

```
/node_modules/
```

iv. Go to 'package.json' and write the code inside the 'scripts' :

```ruby
"start":"node index.js"
``` 

#### For See the Server:

```ruby
node index.js
```
or,
```ruby
nodemon index.js
```
