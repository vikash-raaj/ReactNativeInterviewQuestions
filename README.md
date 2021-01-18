# ReactNativeInterviewQuestions
ReactNativeInterviewQuestions

React Native( Version 0.63.3 )
What is react native

React Native is an open-source mobile application framework, created by Facebook & written in JavaScript. You can build native mobile apps using React Native, which is supportable for both Android, iOS, Web and UWP.
 What is States & Props?

There are two types of data that control or customise a component
Props : Props is short for “properties.
State

Customization of components with different - different ,these parameters is known as Props.

props are set by the parent and they are fixed throughout the lifetime of a component. 
For data that is going to change, we have to use state. It is mutable means a state can change the value at any time.
Ex: Blinking a text
React Native or React Component Lifecycle?

All React class components have their own phases. When an instance of a component is being created and inserted into the DOM, it gets properties,  or props, and from now on they can be accessed using this.props. Then the whole lifecycle ‘thing’ begins.

 A component’s lifecycle can be divided into 4 parts:
Mounting —  an instance of a component is being created and inserted into the DOM.
constructor()
getDerivedStateFromProps()
render()
componentDidMount()
 
Updating — when the React component is born in the browser and grows by receiving new updates. 
getDerivedStateFromProps()
shouldComponentUpdate()
render()
getSnapshotBeforeUpdate()
componentDidUpdate()
 
Unmounting — the component is not needed and gets unmounted.
componentWillUnmount()
 
Error handling — called when there is an error during rendering, in a lifecycle method, or in the constructor of any child component.
State management in React Native ?
   Redux is a javascript library for managing application state.
What is the difference between functional Component & Class Component ? 

        Functional Components                  
                         Class Components                
A functional component is just a plain JavaScript function that accepts props as an argument and returns a React element.
A class component requires you to extend from React. Component and create a render function which returns a React element.
There is no render method used in functional components.
It must have the render() method returning HTML
Also known as Stateless components as they simply accept data and display them in some form , that is they are mainly responsible for rendering UI.
Also known as Stateful components because they implement logic and state.
React lifecycle methods (for example, componentDidMount) cannot be used in functional components.
React lifecycle methods can be used inside class components (for example, componentDidMount).
What is Flat list and Section List?

React Native provides a suite of components for presenting lists of data. Generally, you'll want to use either FlatList or SectionList.

The FlatList component displays a scrolling list of changing, but similar structured, data. FlatList works well for long lists of data, where the number of items might change over time. Unlike the more generic ScrollView, the FlatList only renders elements that are currently showing on the screen, not all the elements at once.

What is JSX?
JSX Stands for JavaScript XML. React and React Native use JSX, a syntax then  you can  write elements inside JavaScript like : <Text>Hello, World</Text>

What is flex?

flex will define how your items are going to “fill” over the available space along your main axis. Space will be divided according to each element's flex property.

Ex: there is three child like color red,blue,green, want to fill the entire screen using flex 1,flex 2,flex 3, then color red will fill ⅙, blue 2/6, and green 3/6.

What is Component?
 Anything you see on the screen is some sort of components
EX: View,Text,Image,Button,ScrollView etc.

What is absolute and Relative Layout?
The position type of an element defines how it is positioned within its parent, 

Relative (default value) By default, an element is positioned relatively. This means an element is positioned according to the normal flow of the layout, and then offset. 
Ex: we insert Text1,Image and then text2 then they show on the screen by relative path like first one is text1, 2nd one is image and ;last thing will show the text2

Absolute  :When positioned absolutely, an element doesn't take part in the normal layout flow. It is instead laid out independent of its siblings. The position is determined based on the top, right, bottom, and left values.

What are the benefits of React Native?
             Learn Once write Everywhere
Cross-platform Development
Open source
Faster Development
Large Community
Live and Hot Reloading
Easy to use
Provides Native Look and Feel 

   12.  What is the difference between react native and react and similarity  ?
    Both, React and React Native uses
React Lifecycle Methods
React State and Props
React Components
Redux Library
React Js:
ReactJs is a JavaScript Library used for developing apps in HTML5 using JavaScript as the developing language
React Native:
React Native is used to develop native mobile apps using JavaScript as the development language.

13. What is mapping and how to use it in react native?
The map() function is used to iterate over an array and manipulate or change data items. In React, the map() function is most commonly used for rendering a list of data to the DOM

The map function is used to show a list of elements from an array. Properly saying, The map() method creates a new array with the results of calling a provided function on every element in the calling array. 

var array = [1, 2, 3, 4];

const map = array.map(element => element * 2);

console.log(map);
// expected output: Array [2, 4, 6, 8]
14.  Difference between 0.6 version and older version?
A Fresh Start
AndroidX Support
CocoaPods by Default
Lean Core Removals
Focus on Accessibility 
There have been many improvements to the accessibility APIs, like announceForAccessibility, plus improvements to roles, action support, flags, and more

What is Babel?
Babel is a JavaScript compiler
Babel is a toolchain that is mainly used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments. Here are the main things Babel can do for you:
Transform syntax
Polyfill features that are missing in your target environment (through @babel/polyfill)
Source code transformations (codemods)
And more! (check out these videos for inspiration)




Redux(4.0.5)

What is redux?
Redux is a JavaScript library for managing and updating  Application States. Using Events called actions.
Need of Redux OR Why do we use Redux?
Redux provides a way to centralize the state of your application.
Suppose, you need to pass data in between such components that don't have any relationship (parent-child), so while making communication between such components, it is difficult to pass data and maintaining them is also a very difficult task.
There are three possible solutions to solve this problem.
Redux
Context API
Hookes - useContext + useReducer	

In such a case redux is very useful because Redux eliminates the need to continuously pass data from one component to another component.
Benefits of using Redux?
Single-Source of Truth
Predictable States
Easy to Maintain
Reusable Code
No need to uplift State
Easy to Debug

 redux.js  4.0.5 VS previous version?(Difference)
Changes
This release includes a memory leak fix, and a fix for removing reducers with replaceReducer and combineReducers.


What are the Redux Core Principles? (Explain by Cake Example)
Store
Action
Reducer
  
Single-Source of Truth 
State is Read-Only
Changes are made with Pure Functions  
1. Single-Source of Truth:
The state of your whole application is stored in an object tree, called Store.
2. State is Read-Only:
The only way to change the state is to dispatch an Action, an object describing what happened.
3. Changes are made with pure functions:
To specify how the state tree is transformed by actions, you write pure Reducers.
How Redux Works - Redux Workflow?
Redux allows you to manage the state of the application using single source of truth, called Store, Any Component can directly access the state from the Store using Subscribe method.
Let's understand the Redux workflow step by step:
Store - Redux offers a solution of storing all your application's state at one place, called store.
Action - Actions can be dispatch based on the Event (e.g. OnClick, OnChange, etc).
Reducer - Reducers are the pure functions which takes the previous state and an action, and return the next state. (Always return new state objects, instead of mutating the previous state).
Subscribe - Any components can easily subscribe to store.
In Redux, components don't communicate directly with each other, but rather all state changes must go through the single source of truth, the store.
 What are the important Redux Terminology?
Store
Action
Reducer
Action Creator
Dispatch
Subscribe
Provider
Connect
  What is Store? How to create Store in React?
A Store is an Object which holds the whole state tree of your application.
import React, { Component } from "react";
import { createStore } from "redux";

const initialState = {
  lang_code: "en",
};

const langReducer = (state = initialState, action) => {
  //make a copy of initialState 
  //(you can also use - Object.assign({}, state))
  let newState = {...state}; 
  if (action.type === "SET_LANGUAGE") {
    newState.lang_code = action.lang_code;
  }
  return newState;
};

const store = createStore(langReducer);

 What is Reducer?
Reducer are pure fucntions which take the previous state of the app and return a new state based on the action passed to it.
Important:  Reducer are pure functions which take the previous state of the app and return a new state based on the action passed to it
You can achieve this using
Object.assign()
Spread (…) operator
const language = (state, action) => {
    let newState = {...state};
    if (action.type == "SET_LANGUAGE") {
        newState.lang_code = action.lang_code;
    } 
    return newState;
}


What is Action?
Actions are plain JavaScript objects and they must have a type property to indicate the type of action to be carried out. They must also have a payload that contains the information that should be worked on by the action.
Actions are dispatched using store.dispatch() method.

 What is an Action Creator?
Action Creator is a function which return an action.
What is Dispatch? 
Dispatch is a method which triggers action with type and payload to Reducer.
What is Subscribe? How you can use it in React App? 
Subscribe is a method which is used to subscribe data/state from Store automatically whenever there will any changes in state.
What is Provider? 
The Provider is a component that has a reference to the Store and provides the data from the Store to the component it wraps.
What is Connect?
Connect is a function that communicates with the Provider.N
What is Pure Functions? 
A pure function is a function which
always return the same output for the same input
has no side effects, means it doesn't change any external state.
Example
const add = (a, b) => a + b // A pure function

 Redux vs Flux?
    Flux is a Design Pattern and Redux is a library.
REDUX
FLUX
Single Store
Multiple Store
Redux is a container for JavaScript apps.
Flux is a container for application state and logic that are registered to callbacks.
It offers interesting features such as writing applications, testing in different environments such as a server, client, etc.
It is an observer pattern that is modified to fit React.
In redux, actions can be functions or promises.
It is a fancy name given to observer patterns and Facebook has developed tools to aid the implementation of these patterns.
Redux is the first choice for web developers because it offers live code editing.
Flux supports actions that are simple JavaScript objects.

Difference between redux, react-redux, redux-thunk, redux-saga?
redux: main core redux library (independent from react)
react-redux: connects your redux store with react components
redux-thunk: a redux middleware which helps you with async actions
redux-saga: a redux middleware library to handle asynchronous action

How to access redux store outside a react component?
You can export the store from the module you called createStore.

  Can we have multiple reducers? Can we combine multiple reducers? if yes, then how?
Yes, we can combine multiple reducers using - combineReducers.
  What is Middleware? Why middleware is used in Redux?
Middleware are being used in redux for extended functionality. it works between dispatching an action, and the moment it reaches to the reducer.
Middleware are used Redux for

logging
crash reporting
routing
asynchronous API calls

What is Redux Thunk? Why do we need Redux Thunk?
Redux Thunk is a middleware.
Redux Thunk allows you to write action creators that return a function instead of an action.
The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met.
Is Redux immutable?
Yes
Is Redux asynchronous?
Without middleware, Redux store only supports synchronous data flow.



                            Flutter(1.22.5)
Q: What Is Flutter?
Flutter is an open-source mobile application development framework (SDK) created by Google for building high-performance apps for iOS and Android, from a single codebase.
Flutter allows you to build beautiful native apps on iOS and Android from a single codebase

Q: Should I learn DART before learning Flutter?
Yes, learn DART before learning Flutter.
Q: What is Dart?
Dart is a general-purpose, object-oriented programming language originally developed by Google
Q: Which is better Flutter or React Native?
Flutter and React Native both are used to develope hybrid native app which run for iOS and Android from a single codebase.
React Native came earlier into market by Facebook (Initial release: March 26, 2015)
Flutter came recently (Initial release date: May 2017), so it is difficult to choose a winner becasue both have good features and community.
it's upto developer which one they prefer the most for developing mobile application for Android and iOS.
 You may also like - Node.js Interview Questions
Q: What are the advantages of Flutter?
Learn Once write Everywhere
Cross-platform Development
Faster Development
Good Community
Live and Hot Reloading
Native Performance
Provids Native Look and Feel
Expressive and Flexible UI
Q: How to Install Flutter?
You can install it any OS like Windows, Linus, MacOS etc
Read Flutter Installation Guildlines Step by Step
Q: What are best editors for Flutter Development?
Android Studio
VS Code
Read Editors for Flutter
Q: How to write your first Flutter App?
Read Flutter Guildlines Step by Step
Q: How many types of widgets are in Flutter?
StatelessWidget 
StatefulWidget 



              TypeScript(4.1.3)
Q: What is TypeScript?
TypeScript is a superset of JavaScript that compiles to plain JavaScript. It is developed and maintained by Microsoft.
Q: What are the types in TypeScript?
There are mainly two types of data types:
Built-in: This includes number, string, boolean, void, null and undefined.
User-defined: It includes enums, classes, interfaces, arrays, and tuple.
//Boolean
let isDone: boolean = true;

//String
let name: string = "Full Stack Tutorials";

//Number
let decimal: number = 10;

//Array
let list: number[] = [1, 2, 3, 4, 5];


Q: What are the Benefits of TypeScript?
It helps in code structuring
Typescript is purely object oriented programming.
It offers a "compiler" that can convert to JavaScript equivalent code.
It has a concept of namespace defined by a "module".
Type checking
Compile time error checking
Code completion and intelligence
Q: What are the features of TypeScript?
tsc --init
extends in tsconfig.json
type vs interface
keyof
Mapped Types
Mixin classes
object vs Object
Transpiling async/await to ES5/ES3
String valued enums
allowJs, checkJs, // @ts-check
Q: How to compile a typescript file via command line?
tsc fileName
//Example
tsc helloworld.ts
Q: What are the Modules in Typescript?
Modules are the way to organize code in TypeScript. Modules contains classes and interfaces. It is same like namespace in C#.
Types of Modules:
Internal Modules
External Modules
There are different types of components of TypeScript:
Language
Compiler
Language Service
Q: Does TypeScript supports function overloading?
Yes, TypeScript does support function overloading but the implementation is a bit different if we compare it to OO languages.



Node.js(12.18.4)

What is Node.js?

Node Js is an open-source, cross-platform JavaScript runtime environment for executing JavaScript code on the server side.

Features/Advantage Node.js

Asynchronous and Event Driven –
All APIs of Node Js are asynchronous. This feature means that if a Node receives a request for some Input/Output operation, it will execute that operation in the background and continue with the processing of other requests. Thus it will not wait for the response from the previous requests.
It's very fast –
Node Js uses the V8 JavaScript Runtime engine, the one which is used by Google Chrome. Node has a wrapper over the JavaScript engine which makes the runtime engine much faster and hence processing of requests within Node.js also becomes faster.
Single Threaded but Highly Scalable –
Node Js uses a single thread model for event looping. The response from these events may or may not reach the server immediately. However, this does not block other operations. Thus making Node.js highly scalable. Traditional servers create limited threads to handle requests while Node.js creates a single thread that provides service to much larger numbers of such requests.
Node js library uses JavaScript –
This is another important aspect of Node Js from the developer’s point of view. The majority of developers are already well-versed in JavaScript. Hence, development in Node.js becomes easier for a developer who knows JavaScript.
Community –
There is an Active and vibrant community for the Node Js framework - The active community always keeps the framework updated with the latest trends in the web development.
No Buffering –
Node js applications never buffer any data. They simply output the data in chunks.
NPM (Node Package Manager) –
NPM stands for Node Package Manager, it comes with node js & allows us to install various Packages for Node js Application.
Node.js REPL (Read Eval Print Loop)
In node.js, REPL is a run-time environment and it is similar to Shell or command prompt in Linux or windows machines. The REPL stands for Read-Eval-Print-Loop and it is very useful when we want to test a simple JavaScript or node.js code snippets.
 
 
 
 
 
 
Type
Description
Read
It reads the input statements provided by user, parse it to JavaScript data structure, and stores it in memory for further operations.
Eval
It will evaluate the parsed JavaScript data structure and return the result.
Print
Whenever the result is ready, then it will print the result.
Loop
Loops the input command until we press Ctrl + C twice to exit from REPL.

1) What is node.js?
Node.js is a Server side scripting which is used to build scalable programs. Its multiple advantages over other server side languages, the prominent being non-blocking I/O.
2) How node.js works?
Node.js works on a v8 environment, it is a virtual machine that utilizes JavaScript as its scripting language and achieves high output via non-blocking I/O and single threaded event loop.
3)  I/O Term ?
I/O is the shorthand for input and output, and it will access anything outside of your application. It will be loaded into the machine memory to run the program, once the application is started.
 
4)  event-driven programming mean?
In computer programming, event driven programming is a programming paradigm in which the flow of the program is determined by events like messages from other programs or threads. It is an application architecture technique divided into two sections 1) Event Selection 2) Event Handling.
5) Where used node.js?
Node.js can be used for the following purposes.
Web applications ( especially real-time web apps )
Network applications
Distributed systems
General purpose applications
6) What is the advantage of using node.js?
It provides an easy way to build scalable network programs
Generally fast
Great concurrency
Asynchronous everything
Almost never blocks
7) What are the two types of API functions in Node.js ?
The two types of API functions in Node.js are
Asynchronous, non-blocking functions
Synchronous, blocking functions
8) Control flow function?
A generic piece of code which runs in between several asynchronous function calls is known as control flow function.
9) Steps “Control Flow” controls the functions calls?
Control the order of execution
Collect data
Limit concurrency
Call the next step in program
10) Why Node.js is single threaded?
For async processing, Node.js was created explicitly as an experiment. It is believed that more performance and scalability can be achieved by doing async processing on a single thread under typical web loads than the typical thread based implementation.
11) Does node run on windows?
Yes – it does. Download the MSI installer from https://nodejs.org/download/
12) Can you access DOM in node?
No, you cannot access DOM in node.
13) Using the event loop what are the tasks that should be done asynchronously?
I/O operations
Heavy computation
Anything requiring blocking
14) Why node.js is quickly gaining attention from JAVA programmers?
Node.js is quickly gaining attention as it is a loop based server for JavaScript. Node.js gives user the ability to write the JavaScript on the server, which has access to things like HTTP stack, file I/O, TCP and databases.
15) What are the two arguments that async.queue takes?
The two arguments that async.queue takes
Task function
Concurrency value
16) What is an event loop in Node.js ?
To process and handle external events and to convert them into callback invocations an event loop is used. So, at I/O calls, node.js can switch from one request to another.
17) Mention the steps by which you can async in Node.js?
By following steps you can async Node.js
First class functions
Function composition
Callback Counters
Event loops
18) pros and cons of Node.js?
Pros:
If your application does not have any CPU intensive computation, you can build it in Javascript top to bottom, even down to the database level if you use JSON storage object DB like MongoDB.
Crawlers receive a full-rendered HTML response, which is far more SEO friendly rather than a single page application or a websockets app run on top of Node.js.
Cons:
Any intensive CPU computation will block node.js responsiveness, so a threaded platform is a better approach.
Using relational database with Node.js is considered less favourable.
19) How Node.js overcomes the problem of blocking of I/O operations?
Node.js solves this problem by putting the event based model at its core, using an event loop instead of threads.
20) What is the difference between Node.js vs Ajax?
The difference between Node.js and Ajax is that, Ajax (short for Asynchronous Javascript and XML) is a client side technology, often used for updating the contents of the page without refreshing it. While,Node.js is Server Side Javascript, used for developing server software. Node.js does not execute in the browser but by the server.
21) What are the Challenges with Node.js ?
Emphasizing on the technical side, it’s a bit of challenge in Node.js to have one process with one thread to scale up on multi core server.
22) What does it mean “non-blocking” in node.js?
In node.js “non-blocking” means that its IO is non-blocking.  Node uses “libuv” to handle its IO in a platform-agnostic way. On windows, it uses completion ports for unix it uses epoll or kqueue etc. So, it makes a non-blocking request and upon a request, it queues it within the event loop which call the JavaScript ‘callback’ on the main JavaScript thread.
23) What is the command that is used in node.js to import external libraries?
Command “require” is used for importing external libraries, for example, “var http=require (“http”)”.  This will load the http library and the single exported object through the http variable.
24) Mention the framework most commonly used in node.js?
“Express” is the most common framework used in node.js.
25) What is ‘Callback’ in node.js?
Callback function is used in node.js to deal with multiple requests made to the server. Like if you have a large file which is going to take a long time for a server to read and if you don’t want a server to get engage in reading that large file while dealing with other requests, call back function is used. Call back function allows the server to deal with pending request first and call a function when it is finished.

Express.js
Q.1) What is Express.js?
Express.js is a free open-source, light-weight node js based web application framework.
It is designed for building (single-page, multi-page, and hybrid) web applications and APIs.
It has been developed by TJ Holowaychuk in 2010 and written in JavaScript.
Express.js Features:
Following are some of the core features of Express framework:
Middlewares: Set up middlewares in order to respond to HTTP/RESTful Requests.
Routing: It is possible to defines a routing table in order to perform different HTTP operations.
Templates: Dynamically renders HTML Pages based on passing arguments to templates.
High Performance: Express prepare a thin layer, therefore, the performance is adequate.
Database Support: Express supports RDBMS as well as NoSQL databases.
MVC Support: Organize the web application into an MVC architecture.
Manages everything from routes to rendering view and preforming HTTP request.
Q.2) How to allow CORS in Express.js (Node.js)? Explain with an Example?
Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources to be requested from another domain/server.
There are mainly three ways you can do this using
res.setHeader() - It allow to set only single header
res.header() OR res.set() - It allow to set multiple headers.
express cors module
Q.3) What is Scaffolding in Express.js?
Scaffolding is creating the skeleton structure of application
There are 2 way to do this:
Express application generator
Yeoman
Q.4) How to enable debugging in express app?
On linux DEBUG=express:*  , node app.js
On windows : set DEBUG=express:* 
node app.js
 
Q.6) What is routing and how routing works in Express.js?
Routing refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, and so on).

Q7. What is Middleware in Express.js?
Middleware functions can perform the following tasks:
Execute any code.
Make changes to the request and the response objects.
End the request-response cycle.
Call the next middleware function in the stack.
Type of Middleware:
Application-level middleware
Router-level middleware
Error-handling middleware
Built-in middleware
Third-party middleware
Q.10) How to implement JWT authentication in Express app ? Explain with an Example?
Create a folder called 'keys' inside project folder.
Install some dependencies as following: npm install jsonwebtoken –-save
Add the login router routes/index.js


MongoDB
Q:- What is MongoDB databases?
MongoDb is NOSQL database, MongoDB is a document database
MongoDB stores data in flexible, JSON-like documents, meaning fields can vary from document to document and data structure can be changed over time
The document model maps to the objects in your application code, making data easy to work with
Ad hoc queries, indexing, and real time aggregation provide powerful ways to access and analyze your data
MongoDB is a distributed database at its core, so high availability, horizontal scaling, and geographic distribution are built in and easy to us
Q:- What do you understand by NoSQL databases?
There is a problem to handle Big data, Unstructured data and Semi Structured data, So NoSQL is answer of all these problems.
NoSQL stands for "Not Only SQL". NoSQL is a type of database that can handle and sort all type of unstructured, messy and complicated data.
Q:- Is MongoDB a NoSQL database?
Yes. MongoDB is a NoSQL database.
Q:- What are the different types of NoSQL databases? Give some example.
NoSQL databases typically fall into one of four categories:
Key-Value Store:
Every item in the database is stored as an attribute name (or "key") together with its value.
#Example: Riak, Voldemort, Amazon S3 (Dynamo) and Redis etc.
Document based databases:
It pairs each key with a complex data structure known as a document. Documents can contain many different key-value pairs, or key-array pairs, or even nested documents.
#Example: MongoDB
Column based Store:
It stores data together as columns instead of rows and are optimized for queries over large datasets.
#Example: Cassandra, HBase etc
Graph base databases
It is used to store information about networks, such as social connections.
#Example: Neo4J and HyperGraphDB etc
Q:- List most popular NoSQL Database [2020]?
Top 3 are the most popular NoSQL database:
MongoDB
DynamoDB
Cassandra
Q:- Which are the different languages supported by MongoDB?
MongoDB provides official driver support for C/C++, C#, Java, Node, Perl, PHP, Python, Ruby, etc.
Q:- Is MongoDB better than other SQL databases? If yes then how?
Yes, MongoDB is better than other SQL databases in terms of following conditions.
Cases:
High Performance -
MongoDB provides high performance data persistence. It supports embedded data models to reduce I/O activity on a database system, as well as indexes for faster queries, and can include keys from embedded documents and arrays
High Availability -
To provide high quality availability, MongoDb’s replication facility (known as replica sets) provide both automatic failover and data redundancy. A replica set is a group of MongoDB servers that maintain the same data set and provide both redundancy and increased data availability
Automatic Scaling -
MongoDB provides horizontal scalability as part of its core functionality. Automatic sharding distributes data across a cluster of machines, while replica sets can provide eventually-consistent reads for low-latency deployments
Schema Less -
JSON data model with dynamic schemas
Semi-Structured/Unstructured -
Best Suited for Semi-Structured/Unstructured Data as well as Structured data also Ad hoc queries, indexing, and real time aggregation provide powerful ways to access and analyze your data
Free -
MongoDB is free and open-source, published under the GNU Affero General Public License
Q:- Why MongoDB is known as best NoSQL database?
MongoDb is the best NoSQL database because, it is:
Document Oriented
Rich Query language
High Performance
Highly Available
Easily Scalable
 You may also like - React.js Interview Questions
Q:- What is mongo in MongoDB?
mongo is an interactive JavaScript shell interface to MongoDB
It provides a powerful interface for system administrators as well as a way for developers to test queries and operations directly with the database.
Q:- What is mongod in MongoDB?
mongod is the MongoDB database server.
The mongod process starts the MongoDB server as a daemon.
The MongoDB server manages data requests and formats and manages background operations
Q:- What is mongos in MongoDB?
The routing and load balancing process that acts an interface between an application and a MongoDB sharded cluster.
Q:- What is a Namespace in MongoDB?
The namespace is a combination of the database name and the name of the collection or index.
Example: [database-name].[collection-or-index-name]
Q:- What is oplog in MongoDB?
oplog stands for operations log.
oplog is a special capped collection which stores an ordered history of all logical operations that modify the data stored in your database.
Q:- What is MongoDB Projection?
MongoDB projection means selecting only the necessary data rather than selecting whole of the data of a document.

//User Collection
{
	"_id" : ObjectId("25bf63380be1d7770c3982af"),
	"name" : "Test 1",
	"email" : "test1@test.com",
	"age" : 22
}
{
	"_id" : ObjectId("12bf63500be1d7770c3982b0"),
	"name" : "Test 2",
	"email" : "test2@test.com",
	"age" : 22
}
{
	"_id" : ObjectId("34bf63650be1d7770c3982b1"),
	"name" : "Test 3",
	"email" : "test3@test.com",
	"age" : 23
}
//To get only name of users for all the documents, we will use the Projection like this:
> db.user.find({}, {"_id": 0, "name": 1});
{ "name" : "Test 1" }
{ "name" : "Test 2" }
{ "name" : "Test 3" }
 
Q:- Does the MongoDB have the Schema?
Yes, MongoDB have the Dynamic Schema so there is no need to define structure to create collections in MongoDB.
Q:- Does MongoDB support primary-key and foreign-key relationship?
No. By Default, MongoDB doesn't support primary key-foreign key relationship.
But, In MonogDB We can achieve primary key-foreign key relationship in following ways:
embedding
referencing
#Example: An address document can be embedded inside user document.

{
   _id: "4f7ee46e08403d063ab0b4f9",
   name: "Harry",
   addresses: [
                {
                  street: "123 Street 1",
                  city: "New Delhi",
                  state: "New Delhi",
                  zip: "12345"
                },
                {
                  street: "Some Other Street",
                  city: "Boston",
                  state: "MA",
                  zip: "12345"
                }
              ]
 }
 
 You may also like - JavaScript Interview Questions
Q:- What is pipeline in MongoDB?
A series of operations in an aggregation process.
The MongoDB aggregation pipeline consists of stages.
Each and evenry stage transforms the documents as they pass through the pipeline
Pipeline stages do not need to produce output documents for each and every input documents.
MongoDB provides the db.collection.aggregate() method.
Note- Pipeline stages can appear multiple times in the pipeline.
There are following possible stages in aggregation pipeline.
$project − It is used to select only specific fields from a collection.
$match − It is used to filter out the document based on some conditions.
$group − It is used to group the documents.
$sort − It is used to sorts the documents.
$skip − It is used to skip documents.
$limit − It is used to limit the documents.
$unwind − It is used to unwind documents.
Q:- Does MongoDB need a lot of RAM?
No It can also be run on small amount of RAM because it dynamically allocates and de-allocates RAM according to the requirement of the processes.
Q:- Explain the structure of ObjectID in MongoDB.
ObjectId is a 12-byte BSON type.
ObjectID consists of
4 bytes value representing seconds
3 byte machine identifier
2 byte process id
3 byte counter
Q:- Is it true that MongoDB uses BSON to represent document structure?
Yes.
Q:- What are Indexes in MongoDB?
In MongoDB, Indexes are used to execute query efficiently.
It imporoves the search performance but the same time if you will create too many unnecessary index then it may slow down write operations.
Q:- By default, which index is created by MongoDB for every collection?
By default, the _id collection is created for every collection by MongoDB.
To create an index in the Mongo Shell, use db.collection.createIndex().
Synatx:

db.collection.createIndex(keys, options);
 
#Example:

db.user.createIndex( { name: -1 } );
 
There are following types of Indexes in MongoDB
Single Field
Compound Index
Multikey Index
Geospatial Index
Text Indexes
Hashed Indexes
#Example : Create an Index on a Multiple Fields
The following example creates a compound index on the username field (in ascending order) and the city field (in descending order.)

db.user.createIndex( { "username": 1 , "city": -1 } );
 
NOTE: Order of Index
The order of an index is important for supporting sort() operations using the index.
The createIndex() method has the behaviors described here.
To add or change index options you must drop the index using the dropIndex() method and issue another createIndex() operation with the new options.
If you create an index with one set of options, and then issue the createIndex() method with the same index fields and different options without first dropping the index, createIndex() will not rebuild the existing index with the new options.
If you call multiple createIndex() methods with the same index specification at the same time, only the first operation will succeed, all other operations will have no effect.
Non-background indexing operations will block all other operations on a database.
MongoDB will not create an index on a collection if the index entry for an existing document exceeds the Maximum Index Key Length.
Note:
Use db.collection.createIndex() rather than db.collection.ensureIndex() to create indexes.
Use db.collection.getIndexes() to view the specifications of existing indexes for a collection.
For more details - please visit MongoDB Official Website
Q:- In which language MongoDB is written?
MongoDB is written in C++.
Q:- How to do Transaction/locking in MongoDB?
MonogDB doesn't supports Transaction
MongoDB doesn't use traditional locking or complex transaction with Commit and Rollback.
MongoDB is designed to be light weighted, fast and predictable to its performance. It keeps transaction support simple to enhance performance.
Q:- Why 32 bit version of MongoDB are not preferred?
Because MongoDB uses memory mapped files so when you run a 32-bit build of MongoDB, the total storage size of server is 2 GB. But when you run a 64-bit build of MongoDB, this provides virtually unlimited storage size. So 64-bit is preferred over 32-bit.
Q:- What is explain() in MongoDB ?
In the Mongo shell, you also can retrieve query plan information through the explain() method:

db.collection.explain();
 
 You may also like - MySQL Interview Questions
Q:- Can one MongoDB operation lock more than one databases? If yes, how?
Yes. Operations like copyDatabase(), repairDatabase(), etc. can lock more than one databases involved.
Q:- What is a Storage Engine in MongoDB?
A storage engine is the part of a database that is responsible for managing how data is stored on disk.
#Example, one storage engine might offer better performance for read-heavy workloads, and another might support a higher-throughput for write operations.
You can find the storage engine currently being used.

db.serverStatus().storageEngine;

//Output:
{ "name" : "wiredTiger" }
 
Once it is confirmed that wiredTiger is being used then type

db.serverStatus().wiredTiger;
 
to get all the configuration details of wiredTiger.
Q:- Which are the two storage engines used by MongoDB?
MongoDB uses:
MMAPv1
WiredTiger
Q:- Does MongoDB provide a facility to do text searches? How?
Yes, MongoDB supports creating text indexes to support text search inside string content. This was a new feature which can introduced in version 2.6.
Q:- What is 32-bit nuances?
There is an extra memory mapped file activity with journaling. This will further constrain the limited DB size of 32-bit builds. For now, journaling by default is disabled on 32-bit systems.
Q:- Why does Profiler used in MongoDB?
A tool that, when enabled, keeps a record on all long-running operations in a database's system.profile collection.
The profiler is most often used to diagnose slow queries.
Enable profiling:

db.setProfilingLevel(1);
 
Now let it run for a while. It collects the slow queries ( > 100ms) into a capped collections, so queries go in and if it's full, old queries go out, so don't be surprised that it's a moving target
Find the most recent slow query:

db.system.profile.find().sort({$natural: -1}).limit(1)
 
Q:- What is map-reduce in MongoDB?
A data processing and aggregation paradigm consisting of a "map" phase that selects data and a "reduce" phase that transforms the data. In MongoDB, you can run arbitrary aggregations over data using map-reduce.
For map-reduce operations, MongoDB provides the mapReduce database command.
Q:- Explain the Replication in MongoDB?
Replication is the process of synchronizing data across multiple servers.
Replication provides redundancy and increases data availability with multiple copies of data on different database servers
Replication also allows you to recover from hardware failure and service interruptions.
Replication in more details
Q:- When an object attribute is removed, is it deleted from the store?
Yes, you can remove the attribute and then re-save() the object.
Q:- Are null values allowed in MongoDB?
Yes, but only for the members of an object. A null cannot be added to the database collection as it isn't an object. But {} can be added.
Q:- Does an update fsync to disk immediately?
No. Writes to disk are lazy by default. A write may only hit the disk a couple of seconds later. For example, if the database receives a thousand increments to an object within one second, it will only be flushed to disk once. (Note: fsync options are available both at the command line and via getLastError_old.)
Q:- Why are data files so large?
MongoDB does aggressive preallocation of reserved space to avoid file system fragmentation.
Q:- How long does replica set failover take?
It may take 10-30 seconds for the primary to be declared down by the other members and a new primary to be elected. During this window of time, the cluster is down for primary operations i.e writes and strong consistent reads. However, eventually, consistent queries may be executed to secondaries at any time (in slaveOk mode), including during this window.
Q:- What’s a Master or Primary?
This is a node/member which is currently the primary and processes all writes for the replica set. During a failover event in a replica set, a different member can become primary.
Q:- What’s a Secondary or Slave?
A secondary is a node/member which applies operations from the current primary. This is done by tailing the replication oplog (local.oplog.rs). Replication from primary to secondary is asynchronous, however, the secondary will try to stay as close to current as possible (often this is just a few milliseconds on a LAN).
Q:- Is it required to call ‘getLastError’ to make a write durable?
No. If ‘getLastError’ (aka ‘Safe Mode’) is not called, the server does exactly behave the way as if it has been called. The ‘getLastError’ call simply allows one to get a confirmation that the write operation was successfully committed. Of course, often you will want that confirmation, but the safety of the write and its durability is independent.
Q:- What is sharding in MongoDB?
A database architecture that partitions data by key ranges and distributes the data among two or more database instances. Sharding enables horizontal scaling.
In MongoDB, Sharding is a procedure of storing data records across multiple machines.
It is a MongoDB approach to meet the demands of data growth.
It creates horizontal partition of data in a database or search engine.
Each partition is referred as shard or database shard.
Q:- Should you start out with Sharded or with a Non-Sharded MongoDB environment?
We suggest starting with Non-Sharded for simplicity and quick startup unless your initial data set will not fit on single servers. Upgrading to Sharded from Non-sharded is easy and seamless, so there is not a lot of advantage in setting up Sharding before your data set is large.
Q:- How does Sharding work with replication?
Each Shard is a logical collection of partitioned data. The shard could consist of a single server or a cluster of replicas. Using a replica set for each Shard is highly recommended.
Q:- When will data be on more than one Shard?
MongoDB Sharding is range-based. So all the objects in a collection lie into chunks. Only when there is more than 1 chunk there is an option for multiple Shards to get data. Right now, the default chunk size is 64mb, so you need at least 64mb for migration.
Q:- What happens when a document is updated on a chunk that is being migrated?
The update will go through immediately on the old Shard and then the change will be replicated to the new Shard before ownership transfers.
Q:- What happens when a Shard is down or slow when querying?
If a Shard is down, the query will return an error unless the ‘Partial’ query options is set. If a shard is responding slowly, Mongos will wait for it.
Q:- How do I view connections in MongoDB OR How to Check the current number of connections in MongoDB?

db.serverStatus().connections;

//Output
{"current" : CURRENT_CONNECTION_COUNT, "available" : TOTAL_CONNECTION_COUNTS}
 
Q:- What are the best features OR advantages of Mongodb?
Document-oriented
High performance
High availability
Easy scalability
Rich-query language
Q:- What are the disadvantages of MongoDB?
Document Size:
Max document size is 16 MB.
Transactions:
There is no default transaction support; you need to handle this yourself. So for Transactions based Applications RDBMS is best choice.
Joins:
In MongoDB, it's difficult to represent relationships between data so you end up doing that manually by creating another table to represent the relationship between rows in two or more tables.
Following are some other useful questions related to MongoDB.

Is MongoDB Support Relationship?
Is MongoDB Support Replication?
In MongoDB, What is a namespace?
In which language MongoDB is written?
Do MongoDB databases have tables and schemas?
What types of languages use to work with MongoDB?
Does MongoDB support SQL Server?
Does MongoDB support ACID Transactions?
What is the difference between MongoDB and CouchDB?
What are different between MongoDB and Sql Server databases?
How MongoDB is better than other SQL Server databases?
What are difference between SQL Server and NoSQL Database?
Now days, what makes MongoDB best?
How to create primary/foreign key relationships in MongoDB?
What are 32-bit nuances?
Can MongoDB used for Cache Management?
Why does Profiler use in MongoDB?
In MongoDB, What is a covered query?
In MongoDB, What is Aggregation?
In MongoDB, What is Sharding?
Why MongoDB data files so large (in size)?
In MongoDB, What is GridFS?
Is MongoDB support null values?
In MongoDB, How do I do transactions/locking?
In MongoDB, What is the Master or primary key?
In MongoDB, What is secondary or slave?
In MongoDB, How does sharding work with replication?
In MongoDB, Can I remove old files in the move Chunk directory?
How can I see the connections which you used in mongos?
What are the limitations of MongoDB?
In MongoDB, What is Replication Factor?
In MongoDB, What is dynamic Schema?
In MongoDB, What is BSON and how can restore this file?
In MongoDB, How can you take database backup?
In MongoDB, What is Replication?
In MongoDB, What is the role of 8 Analysers?
In MongoDB, if user removed to object attribute that attribute is deleted from the storage layer? If yes, then how?
In MongoDB, Whether use to safe backup log feature?
In MongoDB, How to update operations immediately sync to disk?
In MongoDB, How to perform transactions/lock?
In MongoDB, How sharding and replication work together?
In MongoDB, How do you configure to cache size for MMAPv1?
Does MongoDB handle application level caching?
Why MongoDB logging so many “Connection Accepted” events?
Does MongoDB run on Amazon EBS?
In MongoDB, How is Query injection and how to handle it?
How can you enter multi line operations in the mongo shell?
How can you access different databases temporarily?
Is mongo shell supported to tab completion?
How can you customize to mongo shell prompt?
Can you edit long shell operations with an external text editor?
What types of locking use in MongoDB?
How do you see the locking status in mongo instances?
Can you perform read/write operation for ever yield lock?
In MongoDB, Which operations lock the database?
In MongoDB, Which commands you use to lock the database?
In MongoDB, Can you lock more than one database at the same time?
How to create Index after every query insert?
How to know, what indexes exist in a collection?
How to determine the size of an index?
What happen when an index does not fit into RAM?





JAVA SCRIPT
What is the difference between Var, Let, Const keyword?
The 2015 version of JavaScript (ES6 - ECMAScript 2015) allows the use of the  const and let.
Const keyword to define a variable that cannot be reassigned, and the 
let keyword to define a variable with restricted scope.
And Var is used to declare all types of variable string,constant, number etc.

Q:- What is JavaScript?
JavaScript(JS) is an object-based, lightweight and cross-platform, high-level, interpreted scripting language.
Q:- Is JavaScript case sensitive language?
Yes, JavaScript is a case-sensitive scripting language. variable's name, keywords, methods, event handlers are all case sensitive.
Q:- What data types are supported in Javascript?
JavaScript provides different data types to hold different types of values.

There are mainly category of two types of data types available in JavaScript.

Primitive data type
Non-primitive (reference) data type
Primitive Data Types:
Boolean
Number
String
Null
Undefined
Symbol
Non-Primitive Data Types:
Object
Array
Q:- What are the pop up boxes available in JavaScript?
Alert Box
Confirm Box
Prompt Box

alert("JavaScript Interview Questions");  // Alert Message

confirm("Are you sure?");  // Return True Or False

prompt("Please enter your name");  // Return user provided input
 You may also like - Advanced JavaScript Interview Questions
Q:- What is the DOM and BOM in JavaScript?
Document Object Model (DOM):
DOM stands for Document Object Model, DOM: This consists of objects that have to deal with the currently loaded page, which is also called the document.

#Example: document

Browser Object Model (BOM):
BOM stands for Browser Object Model. Unlike DOM, there is no standard defined for BOM, hence different browsers implement it in different ways. Typically, the collection of browser objects is collectively known as the Browser Object Model.

BOM is superset of DOM.
#Example: navigator, screen, location, frames,history, XMLHttpRequest etc

Q:- What is the Window in JavaScript?
Window is root global object in JavaScript.
All global JavaScript objects, functions, and variables automatically become members of the window object.

Even the document object (of the HTML DOM) is a property of the window object.


window.document.getElementById("id");

is the same as

document.getElementById("id");
Q:- What is the difference between defer and async?
defer:
defer scripts are executed once the parser has finished it's job. defer scripts also gaurantees the order of execution in which they were added in page.
defer will download the file/script during HTML parsing, execute file/script only when the parser has finished it's job.

async:
async scripts are executed as soon as the script is loaded. async scripts doesn't gaurantees the order of execution in which they were added in page.
async will download the file/script during HTML parsing, and halt the parser and execute the file/script and then again parser start it's job.

Q:- What is Strict mode in JavaScript?
"use strict"; tells browser that JavaScript code should be executed in "strict mode".
Strict mode is a new feature of ECMAScript 5 or ES5.

Benifits of using "use strict"
It makes code debugging more easier.
It eliminates javascript silent errors and throw errors.
use strict enforces strict parsing and error handling.
Strict mode makes it easier to write "secure" JavaScript.
It is a good practice, developer should use - "use strict" mode.
It is supported by all modern browsers.

"use strict";
PI = 3.14;  //Throw and Error because PI is not declared

"use strict";
const PI = 3.14; //Output: 3.14
 You may also like - Node Js Interview Questions And Answers
Q:- How to write comments in JavaScript?
There are two types of comments in JavaScript.

Single Line Comment: It is represented by double forward slash.
Multi Line Comment: It is represented by forward slash with asterisk symbol.

 //var a = 10;  
 //var b = 20;  
 //var c = a * b; //Multiplication of a and b is store in c variable  
 //document.write("Multiplication of " + a + " and " + b + " is " + c);  

function SingleLineComment() {  
	document.write("Example of Single-line Comments in JavaScript!!");  
}  
SingleLineComment();

/*  
 var a = 10;  
 var b = 20;  
 var c = a * b; //Multiplication of a and b is store in c variable  
 document.write("Multiplication of " + a + " and " + b + " is " + c);  
*/  
function MultilineComment() {  
	document.write("Example of Multi-line Comments in JavaScript!!");  
}  
MultilineComment();
Q:- What is the difference between == and ===?
The == operator checks values only whereas === checks values and data type.

Q:- window.onload vs. $(document).ready() method?
The $(document).ready() event occurs as early as the HTML document start loading, while the window.onload event occurs later when all content (e.g. images etc.) has been loaded.


$( document ).ready(function() {
  // Executes when the HTML document is loaded and the DOM is ready
    alert("Document is ready");
});
Or the shorthand version:

$(function() {
   // Executes when the HTML document is loaded and the DOM is ready
    alert("Document is ready");
});

// .load() method deprecated from jQuery 1.8 onward
$(window).on("load", function() {
     // Executes when complete page is fully loaded, including
     // all frames, objects and images
     alert("Window is loaded");
});
Q:- How to handle exceptions in JavaScript?
try lets you test a block of code for errors.

catch lets you handle the error.

throw lets you create custom errors.

finally lets you execute code, after try and catch, regardless of the result.


try {
  eval('alert("Hello world)');
  if(x == "") throw "is empty";
}
catch(error) {
  console.error(error);
  // expected output: SyntaxError: unterminated string literal
  // Note - error messages will vary depending on browser
}
finally {
    //Block of code to be executed regardless of the try/catch result
}

Q:- List some important HTML DOM Mouse Events?
HTML DOM mouse events

onclick
ondblclick
mousemove
mousedown
mouseover
mouseout
mouseup
 You may also like - Javascript ES6 Interview Questions
Q:- How to get the last index of a string in Javascript?
string.length-1 is used to get the last index of a string in Javascript


var myString="FullStackTutorials";
console.log(myString.length-1);

//Output: 17
Q:- How to get the primitive value of a string in Javascript?
In Javascript valueOf() method is used to get the primitive value of a string.


var myVar= "FullStackTutorials!"
console.log(myVar.valueOf());

//Output: FullStackTutorials!
Q:- How can you create an array in Javascript?
There are 3 different ways to create an array in Javascript.

By Array Literal
Example: var myArray = [value1,value2...valueN];

By creating Instance of Array
Example: var myArray = new Array();

By using an Array constructor
Example: var myArray = new Array('value1','value2',...,'valueN');

Q:- How to add an element [Begnning, End, At Specific Position] to an array in JavaScript?
You can use unshift and push function


var myArr = ['Apple', 'Orange', 'Mango'];

myArr.unshift('Pineapple'); // At the Begnning
myArr.push('Strawberries'); // At the end 

console.log(myArr); //  ["Pineapple", "Apple", "Orange", "Mango", "Strawberries"]
You can also use ES6 spread operator


var myArr = ['Apple', 'Orange', 'Mango'];
myArr = ['Pineapple', ...myArr, 'Strawberries'];

console.log(myArr); //  ["Pineapple", "Apple", "Orange", "Mango", "Strawberries"]
You can use splice function add an element into an array at any specific postion.


var myArr = ['Apple', 'Orange', 'Mango'];
myArr.splice(0, 0, "Pineapple");  // At 0th Index
myArr.splice(4, 0, "Strawberries"); // At 4rth Index

console.log(myArr); //  ["Pineapple", "Apple", "Orange", "Mango", "Strawberries"]
Q:- Difference between the substr() and substring() functions in JavaScript?
The substr() function has the form substr(startIndex,length). It returns the substring from startIndex and returns length number of characters.


var s = "FullStackTutorials";
console.log(s.substr(1,4));

//Output: ullS
The substring() function has the form substring(startIndex,endIndex). It returns the substring from startIndex up to endIndex – 1.


var s = "FullStackTutorials";
console.log(s.substring(1,4));

//Output: ull
Q:- Explain Frames in JavaScript?
Frames allow you to divide the page into several rectangular areas and to display a separate document in each rectangle. Each of those rectangles are called a "frame".

Q:- What are the common Errors in JavaScript?
In JavaScript, there are the following three types of errors:

Syntax Error
Runtime Error
Logic Error
 
Q:- Explain Page Re-direction in JavaScript?
Page redirection means moving to another location or the page, using JavaScript at the client side.

Using window.location


window.location = "https://www.fullstacktutorials.com/";   
Using window.location.href


window.location.href = "https://www.fullstacktutorials.com/";   
Using window.location.assign


window.location.assign = "https://www.fullstacktutorials.com/";   
Using window.location.replace


window.location.replace = "https://www.fullstacktutorials.com/";   
using window.open


 window.open("https://www.fullstacktutorials.com/", "OpenWindow", "status = 1, height = 250, width = 250, resizable = 0") 
Q:- What will be the output of 10+20+"30" explain with reason?
Ans: - 3030

Reason: 10 and 20 are integer, So they will be added numerically. And since 30 is a string, So it will be concat and final output will be 3030.

Q:- What will be the output of "30"+20+10 explain with reason?
Ans: - 302010

Reason: Since 30 is a string which is at the starting of expression, So it will be concat with all later values so final output will be 302010.

Q:- Write the output of the following javascript programs?
console.log(typeof undefined == typeof NULL)
true, becasue javascript is a case-sensitive, so typeof NULL is undefined

console.log(typeof undefined == typeof null)
false, becasue typeof null is object
    
Q:- What is Scope? types of Scope in JavaScript?
Scope determines the availability or accessibility or visibility of variables, objects, and functions.
Types of Scope:
There are mainly two type of scope in javascript
Global Scope
Local Scope
Block Scope
Function Scope
Q:- What is the difference between let and var?
The difference between let and var is of Scoping.
let gives you the privilege to declare variables that are limited in scope to the block, statement of expression unlike var.
var is rather a keyword which defines a variable globally regardless of block scope.
The both are very similar when used like the following, outside a function block.

let x = 'JavaScript interview questions';  // globally scoped
var y = 'Advanced JavaScript'; // globally scoped
 
Key Points:
Window Object: However, global variables defined with let will not be added as properties on the global window object.

let x = 'JavaScript interview questions';  // globally scoped
var y = 'Advanced JavaScript'; // globally scoped

console.log(window.x); // undefined
console.log(window.y); // 'Advanced JavaScript'
 
Block Scope: let has block level scope.
Redeclaration: let and const variables cannot be re-declared while var variable can be re-declared in the same scope.

'use strict';
let x = 'Hi, FullStackTutorials';
let x = 'Hello, FullStackTutorials'; // SyntaxError: Identifier 'x' has already been declared
 

'use strict';
var y = 'Hi, FullStackTutorials';
var y = 'Hello, FullStackTutorials'; // No problem, 'y' is replaced.
 
Let's read more about - const in JavaScript ES6
Q:- What is difference between Function Declaration and Function Expression?
Function Declaration:

function myFunc(name) {
 return `Hello ${name}, Welcome to Advanced JavaScript Interview Questions`;
}
console.log(myFunc("User"));

//Output
Hello User, Welcome to Advanced JavaScript Interview Questions
 
Function Expression:
A function expression can be stored in a variable and the variable can be used as a function

var myFunc = function (name) {
 return `Hello ${name}, Welcome to Advanced JavaScript Interview Questions`;
};
console.log(myFunc("User"));

//Output
Hello User, Welcome to Advanced JavaScript Interview Questions
 
There are many benefits of using function expressions
It can be used as Closure
It can be passed as arguments to other Function
It cab be used as Immediately Invoked Function Expressions (IIFE)
Function Expressions can not be Hoisted.
Q:- What is Immediately Invoked Function Expressions (IIFE) in JavaScript?
An IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined.
It is a design pattern which is also known as a Self-Executing Anonymous Function

(function () {
    statements
})();
 
Example

var sum = (function (a,b) {
    return a+b; 
})(2,3); 
console.log(sum); // 5

var sum = ((a,b) => {
    return a+b; 
})(2,3); 
console.log(sum); // 5

(function (a,b) {
    console.log(a+b); 
})(2,3);   // 5
 
Q:- What is Hoisting in JavaScript?
Hoisting is JavaScript's default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function).
variables and function declarations are moved to the top of their scope before code execution.
In JavaScript, a variable can be declared after it has been used. In other words, a variable can be used before it has been declared.

x = 5; 
console.log(x); // Output: 5
var x; 
 
JavaScript only hoists declarations, not initializations.

var x = 5; 
console.log('value is ' + x + ' and '+ y);
var y = 10; 

//Output: value is 5 and undefined
Note - Because variable y is not initialized before it is being used.

 
 You may also like - Javascript ES6 Interview Questions
Q:- Is JavaScript a case sensitive language?
Yes, JavaScript is case sensitive.
Q:- What is functions JavaScript?
1. Anonymous Function - This type of function has no name.

var anonmFunc = function(){
  console.log("Advanced JavaScript Interview Questions and Answers");
}
 
2. Regular Named Function - This function is named properly and specifically.

function myFunc(){
  console.log("Advanced JavaScript Interview Questions and Answers");
}
 
3. Arrow Function - Arrow function (kind of anonymous function) is part of ES6.
Arrow functions is best suited with anything that requires this to be bound to the context, and not the function itself.
Benefits of Arrow Functions
Shorter Syntax
No binding of this

//Regular Function
function myFunc(){
  console.log("Advanced JavaScript Interview Questions and Answers");
}

//Arrow Function
var myFunc = () => {
 console.log("Advanced JavaScript Interview Questions and Answers");
}
 
Unlike a regular function, an arrow function does not bind this. Instead, this is bound lexically (i.e. this keeps it's meaning from its original context).
An arrow function does not have its own this. this value of the enclosing lexical scope is used by arrow functions. So if this is not present in current scope, an arrow function ends up looking into lexical scope.
 You may also like - React.js Interview Questions
Q:- What is Objects in JavaScript?
Object is an unordered collection of data in the form of key:value pairs.
A JavaScript object is an entity having State and Behavior (Properties and Methods).
JavaScript is a prototype based language, so everything is an Object.

//A Simple Object Example

var TV = { 
  Name : "TV Name",
  Price: "15000",
  Color: "Black",
  SwitchON : function (){
		// Code Snippet
  },
  SwitchOFF : function (){
		// Code Snippet
  }
} 
 
Q:- How many ways you can create an Object in JavaScript?
There are many ways to define or create an object in JavaScript.
Different ways of creating an Object in javascript:-
Object Literals
Object Constructor
Object.create Method
using Function
using Class
1. Object Literals:

let obj = {}
 

let person = {
  name: "FullStackTutorials",
  getName: function() {
    return this.name;
  }
};
 
2. Object Constructor:

let person = new Object();
person.name = "FullStackTutorials",
person.getName = function(){
  return this.name ; 
};
 
3. Object.create()

// Using Object.create() method:
let person = Object.create(null);
 

let data = {
  name: "FullStackTutorials",
  getName: function() {
    return this.name;
  }
};
let person = Object.create(data);
 
4. Using Function:

function Person(name){
  this.name = name
  this.getName = function(){
    return this.name
  } 
} 

var obj = new Person("FullStackTutorials");
console.log(obj);
 

//Using Function Prototype

function Person(name) {
  this.name = name;
}
Person.prototype.getName = function() {
  return this.name;
};
 
5. Using Class:
ES6 introduced the class keyword to create classes in JavaScript.

class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  getInfo() {
    console.log(this.name + " Age : " + this.age);
  }
}
let perObj = new Person("Full Stack Tutorials", 25);
 
Q:- What is the difference between Object.create and new Object?
Object.create() method creates a new object, using an existing object as the prototype of the newly created object.

let Person = {
  age : 21,
  getIntro: function () {
    console.log(`Hey Guys, Myself ${this.name}. I am ${this.age} years old!`);
  }
};
let personObj1 = Object.create(Person);
personObj1.name = "Full Stack Tutorials"; // "name" is a property set only on "personObj", not on the "Person".
personObj1.age = 25; // inherited properties can be overwritten
personObj1.getIntro();

let personObj2 = Object.create(Person);
personObj2.getIntro();

//Output 
Hey Guys, Myself Full Stack Tutorials. I am 25 years old!
Hey Guys, Myself undefined. I am 21 years old!
 

var person1 = new Object();
person1.name = "Full Stack Tutorials",
person1.getName = function(){
  return this.name ; 
};

var person2 = new Object();
person2.name = "Full Stack Tutorials",
person2.age = 25,
person2.getName = function(){
  return this.name ; 
};

console.log(person1);
console.log(person2);

//Output
{name: "Full Stack Tutorials", getName: ƒ}
{name: "Full Stack Tutorials", age: 25, getName: ƒ}
 
Q:- How can we compare two Array/Objects in JavaScript. Explain?
Primitives data types like strings and numbers are compared by their value, while objects like arrays, dates, and plain objects are compared by their reference.
The comparison by reference basically checks to see if the objects given refer to the same location in memory.

var a = {};
var b = {};
var c = a;
console.log(a==b);	//false
console.log(a===b);	//false
console.log(a==c);	//true
console.log(a===c);	//true
 
Q:- What is a Closure in JavaScript?
A closure is a feature in JavaScript where an inner function has access to the outer (enclosing) function's variables.
It has access to it's own scope i.e. variables defined between its curly brackets.
It has access to the outer function's variables.
It has access to the global variables.

function outer() {
   var a = 10;
   function inner() {
         var b = 20; 
         console.log(a+b);
    }
   return inner;
}
 
Q:- Write the output of the following javascript programs?

for (var i = 0; i < 5; i++) {
  setTimeout(() => { 
	console.log(i); 
  }, 1000);
}

//Output
(5) 5
 
Reason: It will reference the last value stored in i, which was 5.
There are two solution to resolve this problem
Closure
let
Closure It creates a unique scope for each iteration, storing each unique value of the variable within it's scope.

for (var i = 0; i < 5; i++) {
    (function(x) {
        setTimeout(() => { 
			console.log(x); 
		}, 1000);
    })(i);
}
//Output
0
1
2
3
4
 

for (let i = 0; i < 5; i++) {
  setTimeout(() => { 
	console.log(i); 
  }, 1000);
}

//Output
0
1
2
3
4
 
Reason: let has block level scope so variable i is only seen in the for loop's block scope.
Q:- What is Callback Functions?
A callback function is a function passed into another function as an argument(let’s call this other function "otherFunction"), and the callback function gets executed inside the otherFunction after the function has finished execution.

function doHomeWork(subject, callback) {
  alert(`Starting my ${subject} homework.`);
  callback();
}
function alertFinished(){
  alert('Finished my homework');
}
doHomeWork('Computer Science', alertFinished);
 
Q:- Why do we need Callbacks?
JavaScript is an event driven language. This means that instead of waiting for a response before moving on, JavaScript will keep executing while listening for other events.
Callbacks are a way to make sure certain code doesn't execute until other code has already finished execution.
 You may also like - Node.js Interview Questions and Answers
Q:- What is Prototype?
In JavaScript, objects have a special hidden property [[Prototype]] (as named in the specification), that is either null or references another object. That object is called "Prototype".
Q:- What is Prototypal Inheritance?
That [[Prototype]] has a "magical" meaning. When we want to read a property from object, and it’s missing, JavaScript automatically takes it from the prototype. In programming, such thing is called "prototypal inheritance"
The property [[Prototype]] is internal and hidden, but there are many ways to set it. via __proto__or Object.getPrototypeOf // old-way
obj.__proto__
 
// new-way
Object.getPrototypeOf(obj)
The __proto__ is considered outdated and somewhat deprecated (in browser-only part of the Javascript standard).
The modern methods are:
Object.create(proto[, descriptors]) – creates an empty object with given proto as [[Prototype]] and optional property descriptors.
Object.getPrototypeOf(obj) – returns the [[Prototype]] of obj.
Object.setPrototypeOf(obj, proto) – sets the [[Prototype]] of obj to proto.

var a = { name: "Full Stack Tutorials" };
a.__proto__ === Object.prototype // true
Object.getPrototypeOf(a) === Object.prototype // true

function Foo() {};
var b = new Foo();
b.__proto__ === Foo.prototype
b.__proto__.__proto__ === Object.prototype
 
Q:- What is the difference between classical and prototypal inheritance?
Classical Inheritance: A constructor function instantiates an instance via the new keyword. This new instance inherits properties from a parent class.
Prototypal Inheritance: An instance is created by cloning an existing object that serves as a prototype. This instance—often instantiated using a factory function or "Object.create()"—can benefit from selective inheritance from many different objects.
Q:- What is Promise in JavaScript?
A promise is an object which can be returned synchronously from an asynchronous function.
Promise overcome the problem of callback hell.
Promise States:
Fulfilled: onFulfilled() will be called (e.g. resolve() was called).
Rejected: onRejected() will be called (e.g. reject() was called).
Pending: initial state, neither fulfilled nor rejected.
Promise Consumers: then, catch, finally

var promise = new Promise(function(resolve, reject) { 
const A = "fullstacktutorials"; 
const B = "fullstacktutorials"
if(A === B) { 
	resolve(); 
} else { 
	reject(); 
} 
}); 

promise. 
	then(function () { 
		console.log('Success, Your promise has been resolved successfully'); 
	}). 
	catch(function () { 
		console.log('Something went wrong!'); 
	}); 
 
Example:- Write a function compareToTen that takes a number as an argument and returns a Promise that tests if the value is less than or greater than the value 10.

const compareToTen = (num) => {
  p = new Promise((resolve, reject) => {
    if(num > 10) {
      resolve(num + " is greater than 10, success!")
    } else {
      reject(num + " is less than 10, error!")
    }
  })
  return p
}

compareToTen(15)
  .then(result => console.log(result))
  .catch(error => console.log(error))
  
compareToTen(8)
  .then(result => console.log(result))
  .catch(error => console.log(error)) 
 
Q:- What is the difference between call and apply?
apply():
The apply() method calls a function with a given this value, and arguments provided as an array.
Syntax: fun.apply(thisArg, [argsArray])
call():
The call() method calls a function with a given this value and arguments provided individually
Syntax: fun.call(thisArg[, arg1[, arg2[, ...]]])

function myFunction(name, profession) {
    console.log("My name is " + name + " and I am a " + profession +".");
}
myFunction("John", "Developer");
myFunction.apply(this, ["Ajay", "Designer"]);
myFunction.call(this, "Ravi", "Blogger");

//Output:
My name is John and I am a Developer.
My name is Ajay and I am a Designer.
My name is Ravi and I am a Blogger.

 
A useful mnemonic is "A for array and C for comma."
bind():
bind allows you to set the this value now while allowing you to execute the function in the future, because it returns a new function object.
Syntax: fun.bind(thisArg[, arg1[, arg2[, ...]]])
Q:- What is the spread operator in JavaScript?
The spread operator (…) is a new operator introduced in ES6. It allows the expansion of an iterable (e.g., Array) into its constituent elements.

var childArr = [1, 2, 3];
var finalArr = [...childArr, 4, 5, 6];

console.log(finalArr); 
//Output:  [1, 2, 3, 4, 5, 6];
 
Q:- Remove the duplicate elements from the Array?
Using ES6 - Spread & Set Operator
Using jQuery each function
1. Using ES6 - Spread & Set Operator:

var numbers = [1, 2, 3, 4, 5, 5, 5, 5, 5, 5];

function removeDuplicates(array) {
  return [...new Set(array)];
}

console.log(removeDuplicates(numbers)); // [1, 2, 3, 4, 5]
 
Set was introduced in ES6: They can't have duplicate Items.
After we have done that, we simply convert the Set back to an array by using the spread operator.
2. Using jQuery each function:

var names = ["Mike","Matt","Nancy","Adam","Jenny","Nancy","Carl"];
var uniqueNames = [];
$.each(names, function(i, el){
	if($.inArray(el, uniqueNames) === -1) {
		uniqueNames.push(el);
	}
});
console.log(uniqueNames); // ["Mike", "Matt", "Nancy", "Adam", "Jenny", "Carl"]
 
Q:- What are the advantages of using JavaScript?
Following are the advantages of using JavaScript:
Lightweight: JavaScript can be executed within the user’s browser without having to communicate with the server, saving on bandwidth.
Speed: Client-side JavaScript is very fast because it can be run immediately within the client-side browser.
Simplicity: JavaScript is relatively simple to learn and implement.
Versatile: JavaScript supports multiple programming paradigms—object-oriented, imperative, and functional programming and can be used on both front-end and server-side technologies.
Interactivity: Because tasks can be completed within the browser without communicating with the server, JavaScript can create a smooth "desktop-like" experience for the end user.
Rich Interfaces: From drag-and-drop blocks to stylized sliders, there are numerous ways that JavaScript can be used to enhance a website’s UI/UX.
Prototypal Inheritance: Objects can inherit from other objects, which makes JavaScript so simple, powerful, and great for dynamic applications.
Platform Independent: JavaScript is platform independed language. Any JavaScript-enabled browser can understand and interpreted JavaScript code.
Q:- What is JavaScript Design Patterns?
Design patterns are advanced object-oriented solutions to commonly occurring software problems.
Creational Design Patterns:
As the name suggests, these patterns are for handling object creational mechanisms.
Constructor pattern
Factory pattern
Prototype pattern
Singleton pattern
Structural Design Patterns:
This pattern helps to obtain new functionalities without tampering with the existing ones.
Adapter
Bridge
Composite
Decorator
Facade
Flyweight
Proxy
Behavioral Design Patterns:
These patterns are concerned with improving communication between dissimilar objects
Iterator pattern
Observer pattern
Template pattern
Strategy pattern
State pattern
Command pattern
Q:- Does JavaScript support Method Overloading?
No, JavaScript does not support overloading!. JavaScript supports overriding not overloading.

function getSum(n1, n2, n3) {
    return n1 + n2 + n3;
}
function getSum(n1, n2) {
    return n1 + n2;
}
var sum = getSum(2, 3, 10);
console.log(sum); // 5
 
If you will define two or more functions with the same name, the last one will override the previously defined functions and when a call will be made to the function, the last defined function will get executed.
Q:- Why typeof null return object in JavaScript?
Yes, it's true. since null is a primitive datatype still typeof null return object.

typeof null // "object" (not "null" for some legacy reasons)
 
Reason:
This is a kind of bug in javascript which can't be fixed.
In the inital release of JavaScript, values were represented as a combination of
Tag Type
Actual Value
tag refering for object and null was same, that's why typeof null return object.
                 Xmarian
What is Xamarin?
Xamarin is a type of Microsoft owned San Francisco based company. This type of company is founded in May 2011. The developers can use Xamarin tools to write the native Android, iOS and the Window apps with the native user interface. The Xamarin was being developed by the engineers who also created Mono. According to Xamarin, it was being noted that over 1.4 million developers were using the Xamarin products in the 120 countries. There are some of the Xamarin interview questions and answers that will help you a lot.
Xamarin is very much beneficial for app developers. This is because if the developers are developing different apps for different platforms, then they have to wait for a considerable amount of time. In this way, the company may suffer a lot. But the Xamarin will help to reduce the development time and the efforts because it will let you built cross-platform apps.
 
 DOWNLOAD XAMARIN INTERVIEW QUESTIONS PDF
Below are the list of Best Xamarin Interview Questions and Answers
1) What is Xamarin?
Xamarin is a type of cross-platform development technology, where we can build the native user interface for the IOS, Android and the Windows phone. Xamarin gets its name from the Tamarin monkey where T has been replaced with an X.
 
2) What is Xamarin .forms?
A Xamarin .forms is a type of a framework that helps to allow the developers to build the cross-platform applications for the Android, iOS, and Windows.
3) What are the uses of Xamarin?
Xamarin provides all the flexibility to write the core logic using the C# and also provides the extensibility to design the native user interface for each of the platform.
4) What is Xamarin test cloud?
Xamarin test cloud allows testing a mobile application on diverse devices. Test cloud is also for automated testing on many real devices simultaneously.
5) What is data binding in Xamarin?
Data binding is the type of technique that is used to automatically synchronize the data source with the user interface. When the data binding is done and the data or your business model changes, then it reflects the changes automatically to the UI elements and the vice versa.
6) What are the types of a programming language that support Xamarin development?
Xamarin is unique in the sense that it helps in offering a single language that includes C#, class library and runtime. These types of languages work across all three mobile platforms that are iOS, Android and Windows.
7) What are the types of elements that are used in the Xamarin?
The following are the types of elements that are used in the Xamarin:
C# language
Mono .net framework
Compiler
IDE tools
8) What are the type of apps that use the Xamarin?
There are different types of apps that use the Xamarin and they are:
OLO – An online platform to order food
The world bank survey app – An app for the global survey
Storyo – An app that helps to create videos from picture
Freshdirect – Your friendly online grocer
Insightly – A comprehensive CRM and project management application
Just giving – a philanthropic Interface
Evolve – The all in one event based informative app
Super Giant Games – PC games that are compatible with iPhones
Skulls of Shogun – Another multi-platform gaming app
Thermo fisher scientific – An app that blends science a lot
9) What are the reason to use Xamarin for cross-platform development?
The following are some of the reasons to use Xamarin for cross-platform development:
Less to learn
No limits
Faster time to market
Fewer Bugs
Readiness for future
10) What are the types of apps that are built with Xamarin?
The followings are the 5 types of apps that are built with Xamarin- goal 2014 football manager, the secret society, iLearn for kids, parental access and Toolwiz cleaner.
11) What is XAML?
XAML stands for the Extensible Application Markup Language. XAML allows defining the user interface in Xamarin. Forms application use the markup language rather than code.
12) What are the advantages of XAML?
There are many advantages to using XAML. Some main benefits are:
XAML is often more crisp and precise than a similar code.
XAML gives a clean division between an application and its code. Thus, it enables a clear developer-designer workflow.
XAML has the parent-child hierarchy of user-interface objects with greater visual simplicity.
13) What are the different kinds of pages are present in the Xamarin .forms?
The following are some of the different pages that are present in the Xamarin .forms:
Content page – this type of the page displays a single view, often a container such as a stack layout or the scroll view.
Master-Detail page – this type of page manages two types of panes of information.
Navigation page – a page that manages the navigation and the user experiences as a stack of other pages
Tabbed page – this page allows the navigation of the children pages using the tab.
Templated page – a page that helps to display the full page content with a control template and the base class for the content page.
Carousel page – a page allowing the swipe gestures between the subpages such as a gallery.
14) What are the different types of layout control present in the Xamarin .forms?
There are different types of layout controls present in the Xamarin .forms. Some of them are:
Content presenter
Content view
Frame
Scroll view
Template view
Absolute layout
Grid
Relative layout
Stack layout
15) How to set up the Xamarin?
The following are the 4 simple steps to set up the Xamarin:
Download the Xamarin installer
Run the installer
Configure it
Activation of Xamarin
16) What are the products of Xamarin?
The following are the main products of the Xamarin:
Xamarin platform
Xamarin .forms
Xamarin test clouds
Xamarin for visual studio
Xamarin Studio
Xamarin .mac
.Net mobility scanner
Robo VM
17) What are the different types of data binding modes in Xamarin?
The following are the different types of data binding modes in Xamarin:
Default
One way – changes in the source affects the target
One way to the source – changes in the target affect the source
Two way – changes in the source and target affect each other
18) What are the different types of scenario used in the Xamarin .forms?
The following are the different types of scenarios used in the Xamarin .forms:
View to view bindings
Binding with the models
Backward bindings
Binding with the collections
19) What are the uses of the data pages in the Xamarin .forms?
The data pages help the developers to quickly and easily consume a supported data source and then render it by using the UI scaffolding. One can customize it with the themes.
20) What are the differences between Xamarin and mono?
Xamarin
Mono
Xamarin is one of the most powerful solutions for building awesome apps.
If you want to build an app for a single platform, then you need to have a native platform.
Using the Xamarin you can create native apps for multiple platforms via the same IDE, API’s and language.
Native mobile apps are built on Android, Java, IOS, and Windows.
Using Xamarin, entrepreneurs can skip the extra development time for each platform.
Using Mono, entrepreneurs cannot skip the extra development time for each platform.
Xamarin apps are mainly accessible for wider ranges at a lower cost.
Mono is accessible for the wider ranges at a higher cost.
 
 
 
 
 
 
 
    

