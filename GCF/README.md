# REST API USING EXPRESS IN GOOGLE CLOUD FUNCTIONS


### STEP-1

  - Initialize git repo
    ```sh
    $ git init
    ```
  - After installing firebase tools,run 
    ```sh
    $ firebase init
    ```
    choose cloud functions and follow setup

### STEP-2
  - Add express router in index.js
     ```sh
     // index.js
     const functions = require('firebase-functions');
     const app = require('express')
     const urlencodedParser = express.urlencoded({ extended: false });
     app.get('/', function (req, res) {
        res.send('Hello World!');
    });
    .
    . // other routes
    .
    ```
  - Export router as
     ```sh
        exports.api = functions.https.onRequest(app);
    ```
  

### STEP-3
  - Make changes and add essential code
  - when work is done 
    ```sh
    $ firebase deploy --only functions
    ```
    





  
