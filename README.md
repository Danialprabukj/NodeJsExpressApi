## NodeJsExpressApi
To create APIs using Node, Express and MongoDB.

Need Mondgod and Mongosh databases.
https://www.mongodb.com/try/download/shell

### `mongod`
This command will start your mongodb server on your machine. If you have not start the mongodb on
your then you will get database connection error when run node server.

 In the project directory, you can run:

### `npm install express body-parser mongoose nodemon --save`

This will install the dependencies in the package.json file.

### `npm install`

This will install the dependencies inside `node_modules`


"start": "nodemon server"
Add this line inside the script in the package.json file.
### `node server.js` OR `nodemon start`

Runs the app in the development mode.<br>
Open [http://localhost:4000](http://localhost:4000) to view it in the browser.

### `npm start`
This will run the application

Sometimes Database won't connect , neither all the code were right.

Error:- 
Could not connect to the database. MongooseServerSelectionError: connect ECONNREFUSED ::1:27017
    at _handleConnectionErrors (D:\NodeJsExpressApi-master\node_modules\mongoose\lib\connection.js:792:11)    
    at NativeConnection.openUri (D:\NodeJsExpressApi-master\node_modules\mongoose\lib\connection.js:767:11) { 
  reason: TopologyDescription {
    type: 'Unknown',
    servers: Map(1) { 'localhost:27017' => [ServerDescription] },
    stale: false,
    compatible: true,
    heartbeatFrequencyMS: 10000,
    localThresholdMS: 15,
    setName: null,
    maxElectionId: null,
    maxSetVersion: null,
    commonWireVersion: 0,
    logicalSessionTimeoutMinutes: null
  },
  code: undefined
  
To fix this:-
### `mongod --ipv6`  
By default mongo disables ipv6.
Refer this link :- https://stackoverflow.com/questions/69840504/mongooseserverselectionerror-connect-econnrefused-127017

Reference:- 
https://medium.com/@rahulguptalive/how-to-build-simple-restful-crud-api-with-nodejs-expressjs-and-mongodb-2d25a0e27937

Github link:-
https://github.com/rahulguptafullstack/NodeJsExpressApi
