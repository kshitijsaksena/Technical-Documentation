## How to use axios for POST request in Node.js

### Axios
Axios is a promise-based HTTP client for Node.js. It can be used to send HTTP request from a Node server. As it supports promises it can handle the operations asynchronously, making it a preffered option for modern web development.

### Setting up the environment to use Axios
- Before we move to making POST requests, let’s ensure that we have Node.js and Axios installed in our environment. You can install Node.js from the official website ([https://nodejs.org/](https://nodejs.org/en/download)).
- Create a new project directory. Open command prompt and navigate to the path of this newly created directory. Install Axios via npm, the Node.js package manager, by running the following command in your terminal:
```bash
npm install axios
```
### Making a POST request using Axios
- Now open the project in your favourite code editor and create an index.js file which we will use for Axios code.
- First we need to require axios to our code to be able to use it.
```javascript
const axios = require('axios');
```
- To make a POST request we can axios.post(url,data,config) function. This takes three arguments
  - url: url of the api
  - data: In post request we send data along with request. This data has to be sent in json format.
  - config: There are many config that are added to the request. You can read the configs supported in this on ([axios docs](https://axios-http.com/docs/req_config)).
- Here's an example, we are making a POST request to https://example.com/api/resource with an object containing the name and email fields in the request body. The .then() method handles the successful response, while the .catch() method catches any errors that occur during the request.
```javascript
axios.post('https://example.com/api/resource', {
  name: 'John Doe',
  email: 'john@example.com'
})
.then(response => {
  console.log('Response:', response.data);
})
.catch(error => {
  console.error('Error:', error);
});
```
