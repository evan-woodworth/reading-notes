# Reading Notes
A collection of notes and take-aways throughout my Code 401 journey.
## Code 401 - Advanced Software Development

- [Articles](#articles)
- [Videos](#videos)
- [General Notes](#general-notes)

## Articles

- [Solving Problems](#solving-problems)
- [Act like you make $1000/hr](#act-like-you-make)
- [How to think like a programmer](#how-to-think-like)
- [The 5 Whys](#the-5-whys)

### Solving Problems
[source](https://simpleprogrammer.com/solving-problems-breaking-it-down/) -John Sonmez

When solving programming problems, it is important to understand the problem before you ever try to write code for a solution. The author of this article provides the following steps to follow for most problems:

1. Read the problem completely twice.
2. Solve the problem manually with 3 sets of sample data.
3. Optimize the manual steps.
4. Write the manual steps as comments or psuedo-code.
5. Replace the comments or psuedo-code with real code.
6. Optimize the real code.

The overall emphasis here is to put as much thought and attention into understanding the problem, breaking it down into manageable pieces, understanding the steps that need to happen to solve each piece, optimizing those steps for simplicity and ease of understanding.

### Act like you make $1000/hr
[source](https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d) -Anthony Moore

This article explains the benefits of spending your time wisely. The overriding suggestion is to consider your time to be worth $1000/hr, and judge each moment by whether or not is living up to that figure.

An interesting point that the author makes is that you should say "no" to things that are either not worth your time or don't work towards achieving your goals. By overextending yourself, you can take away from the things that you really need to focus on.

Another point of interest is that you should stay focused, rather than allowing yourself to get lost in something. The suggestion is that you should always strive to pay attention to what you are doing and why, so that you don't get distracted or bogged down by meaningless details. The author states "If you don't manage your time, it will manage you."

### How to think like a programmer
[source](https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2/) -Richard Reis

Thinking like a programmer means being able to more effectively solve problems. This means avoiding common pitfalls like getting stuck in a loop of trying solutions until something fits, and establishing a framework from which you can navigate any problem, no matter the complexity.

The suggested steps are:

1. Understand

    Use whatever approach you need to in order ensure that you understand the problem. Write it out, diagram, talk it over with someone or something, do what you need.

2. Plan

    Once you understand the problem, you need to plan your solution. Take the time to identify how you can get from point a to point b. An example provided by the author is "Given input X, what are the steps necessary to return output Y?"

3. Divide

    This step is both straight-forward and essential. Break the problem into smaller, more easily solved problems, then connect the solutions together.

4. Stuck?

    If you try and try, but can't find the solution to a problem, the author three very useful suggestions:
    - Debug: Take a look at each step of your solution to ensure that it works as intended.
    - Reassess: Try approaching the problem differently.
    - Research: Chances are, someone has probably already solved a similar problem.

### The 5 Whys
[source](https://www.mindtools.com/pages/article/newTMC_5W.htm)

This article explains a method of addressing problems that require more than just a "quick fix". The overall idea is to gather a group of subject-matter experts to "go and see" the problem in action, evaluate what the problem appears to be, then ask "why?" until they get to the root of the problem. Then, an effective counter-measure can be identified and employed to prevent the problem from happening again in the future.

Here's an example they provided of what that process might look like:

![5-whys-diagram](./img/5-whys-single-lane.png)

A couple of useful tips that they provided are:
- The "5" is just a suggestion, more or less "why's" may be needed.
- While the immediate answer to a "why" may fall directly on someone's actions or lack thereof, the 5 Whys process enables you to keep asking why until you can find an organizational problem.

## Videos

- [what the heck is the event loop anyway](#what-the-heck-is-the)
- [The Super Mario Effect](#the-super-mario-effect)

### what the heck is the event loop anyway
[source](https://www.youtube.com/watch?v=8aGhZQkoFbQ)

This video explained how JavaScript interacts with the browser to effectively let more than one thing happen at a time. This is an important concept, because JavaScript itself can only run one thing at a time, which would potentially drastically interfere with a user's experience.

Essentially, as asynchronous callbacks are executed, they get passed to a web api, which the browser keeps track of and handles independently of the JavaScript stack. When the conditions are met for the callback, it is passed to the callback queue, where it waits its turn to be sent back to the JavaScript stack. The event loop waits until the stack is empty, then sends the first item in the callback queue to the stack.

### The Super Mario Effect
[source](https://www.youtube.com/watch?v=9vJRopau0g0)

In this video, Mark Rober explains how changing your changing your reaction to failure can ultimately lead to success. He used an example set of data that he collected to show that people who are not concerned with the negative ramifications of failure can bounce right back and try again until they get it right. He then gave many examples from his own life and experiences, reinforcing the idea that you should embrace failure and learn from it, rather than be ashamed or give up.

## General Notes

 - [Class 01 Reading](#class-01-reading)
 - [Class 02 Reading](#class-02-reading)
 - [Class 03 Reading](#class-03-reading)
 - [Class 04 Reading](#class-04-reading)

### Class 01 Reading

1. Describe (in plain English) what Array.map() does  
Array.map() runs each element of an array through a function, and populates a new array with the results.
2. Describe (in plain English) what Array.reduce() does  
Array.reduce() runs each element of an array through a function, producing one accumulated result.
3. Provide code snippets showing how to use superagent() to fetch data from a URL and log the result
   - With normal Promise .then() syntax
    ```javascript
    superagent.get('http://someurl')
    .then(result => {
        console.log(result)
    })
    .catch(err => console.error(err));
    ```
   - Again with async / await syntax
    ```javascript
    async () => {
        try {
            const result = await superagent.get('http://someurl');
            console.log(result);
        } catch (err) {
            console.error(err);
        }
    }
    ```
4. Explain promises as though you were mentoring a Code 301 level student  
Promises represent an asynchronous function call's "promise" to return data at some point in the future, allowing other code to be executed in the meantime. A promise can be assigned to a handler, and a pending promise can return as "fullfilled", providing a value, or "rejected", providing an error definition.
5. Are all callback functions considered to be Asynchronous? Why or Why Not?  
A callback function can be either synchronous or asynchronous, depending on how it is called.

### Class 02 Reading

1. What’s the difference between PUT and PATCH?  
PUT updates an entire resource or creates a new one if it doesn't exist, whereas PATCH updates a partial resource. Using PUT, you'd have to include all of the information in the resource, including the information that doesn't change. With PATCH, you would only have to provide the information that you want to change.
2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server
   - [JSONPlaceholder](https://jsonplaceholder.typicode.com/) - Free fake API for testing and prototyping.
   - [REQ RES](https://reqres.in/) - A hosted REST-API ready to respond to your AJAX requests.
   - [Fake JSON API](https://mocki.io/fake-json-api) - Access fake APIs with dummy data, or create your own fake JSON API.
3. Compare and contrast Swagger and APIDoc.js  
Swagger holds an entire suite of products and tools for API development, for individuals and teams alike. APIDoc.js allows for API documentation generation for comments in your source code.
4. Which HTTP status codes should be sent with each type of (un)successful API call?  
There are numerous codes in the 300's to 500's. They can be found [here](https://www.ibm.com/docs/ru/qradar-common?topic=overview-api-error-messages).
5. Compare and contrast SOAP and ReST  
Some of the major differences include security, bandwidth, and flexibility. SOAP needs more bandwidth, requires advanced security, and is overall much more strict in implementation. The following diagram was pulled from [parasoft.com](https://www.parasoft.com/blog/web-api-vs-web-services-microservices-basics-differences/)  
![soap-vs-rest](./img/soap-vs-rest.png)

#### Vocabulary

| Term | Definition | Source |
|--|--|--|
| Web Server | "A web server is a computer that runs websites. It's a computer program that distributes web pages as they are requisitioned. The basic objective of the web server is to store, process and deliver web pages to the users." | [economictimes](https://economictimes.indiatimes.com/definition/web-server) |
| Express | "Express is a popular unopinionated web framework, written in JavaScript and hosted within the Node. js runtime environment." | [mozilla](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs#:~:text=Express%20is%20a%20popular%20unopinionated,web%20development%20and%20deployment%20tasks.) |
| Routing | "Routing is the process of selecting a path for traffic in a network or between or across multiple networks." | [wikipedia](https://en.wikipedia.org/wiki/Routing) |
| WRRC | Web Request Response Cycle - "The request/response cycle traces how a user's request flows through the app." | [codecademy](https://www.codecademy.com/articles/request-response-cycle-static) |

### Class 03 Reading

1. Name 3 real world use cases where you’d want to change the request with custom middleware  
Authentication, logging, error handling
2. True or false: The route handler is middleware?  
False
3. In what ways can a middleware function end the process and send data to the browser?  
With any of the response functions, such as res.send, res.json, etc.
4. At what point in the request lifecycle can you “inject” middleware?  
At any point before a request has been completed.
5. What can cause express to error with “Request headers sent twice, cannot start a second response”  
"The error "Error: Can't set headers after they are sent." means that you're already in the Body or Finished state, but some function tried to set a header or statusCode. When you see this error, try to look for anything that tries to send a header after some of the body has already been written. For example, look for callbacks that are accidentally called twice, or any error that happens after the body is sent." -from a stack overflow [response](https://stackoverflow.com/questions/7042340/error-cant-set-headers-after-they-are-sent-to-the-client)

### Class 04 Reading

1. Name 3 advantages to Test Driven Development  
More comprehensive testing, focused productivity, better modularization.
2. In what case would you need to use beforeEach() or afterEach() in a test suite?  
When you are testing data models.
3. What is one downside of Test Driven Development  
A considerable increase in work during early development.
4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?  
According to [Justin Robertson](https://www.toptal.com/javascript/es6-class-chaos-keeps-js-developer-up), "The most important difference between class- and prototype-based inheritance is that a class defines a type which can be instantiated at runtime, whereas a prototype is itself an object instance."
5. Why REST?  
REST is highly flexible and reliable. Data is not tied to resources or methods, and data should be relatively consistent with future requests, making it easily cacheable.

#### Vocabulary

| Term | Definition | source |
|-|-|-|
| functional programming | "...a programming paradigm where programs are constructed by applying and composing functions. It is a declarative programming paradigm in which function definitions are trees of expressions that map values to other values, rather than a sequence of imperative statements which update the running state of the program." | [wikipedia](https://en.wikipedia.org/wiki/Functional_programming) |
| object-oriented programming (OOP) | "Object-oriented programming (OOP) is a computer programming model that organizes software design around data, or objects, rather than functions and logic." | [techtarget.com](https://searchapparchitecture.techtarget.com/definition/object-oriented-programming-OOP#:~:text=Object%2Doriented%20programming%20(OOP)%20is%20a%20computer%20programming%20model,rather%20than%20functions%20and%20logic.&text=Once%20an%20object%20is%20known,sequences%20that%20can%20manipulate%20it.) |
| class | "In object-oriented programming, a class is an extensible program-code-template for creating objects, providing initial values for state and implementations of behavior." | [wikipedia](Wikipedia) |
| super | A keyword use to call methods from a parent class. | |
| this | A keyword referring to the instance that is using it. | |
| Test Driven Development (TDD) | A style of programming wherein tests are written first, to fail, and code is written afterwards to make the tests pass. | |
| Jest | "Jest is a JavaScript testing framework designed to ensure correctness of any JavaScript codebase." | [jestjs.io](https://jestjs.io) |
| Continuous Integration (CI) | "... the practice of automating the integration of code changes from multiple contributors into a single software project." | [atlassian.com](https://www.atlassian.com) |
| REST | "REST defines a set of constraints for how the architecture of an Internet-scale distributed hypermedia system, such as the Web, should behave." Those constraints are: Client–server architecture, Statelessness, Cacheability, Layered system, Code on demand (optional), and Uniform interface. | [wikipedia](https://en.wikipedia.org/wiki/Representational_state_transfer) |
| Data Model | "an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities." | [wikipedia](https://en.wikipedia.org/wiki/Data_model) |

