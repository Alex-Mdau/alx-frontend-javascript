ES6 Promises

This Directory contains JavaScript code for working with ES6 Promises. It includes various tasks that demonstrate the usage of promises and related concepts. Each task is implemented in a separate file.

Task Details
0. Keep every promise you make and only make promises you can keep

Implement the function getResponseFromAPI() that returns a Promise. Example usage:

javascript

import getResponseFromAPI from './0-promise.js';

const response = getResponseFromAPI();
console.log(response instanceof Promise);

1. Don't make a promise...if you know you can't keep it

Implement the function getFullResponseFromAPI(success) that returns a Promise. Example usage:

javascript

import getFullResponseFromAPI from './1-promise.js';

console.log(getFullResponseFromAPI(true));
console.log(getFullResponseFromAPI(false));

2. Catch me if you can!

Implement the function handleResponseFromAPI(promise) that appends three handlers to the given promise. Example usage:

javascript

import handleResponseFromAPI from './2-then.js';

const promise = Promise.resolve();
handleResponseFromAPI(promise);

3. Handle multiple successful promises

Implement the function handleMultiplePromises() that takes in two promises and returns a Promise that resolves to an array of the resolved values of the two input promises. Example usage:

javascript

import handleMultiplePromises from './3-all.js';

const promise1 = Promise.resolve('Promise 1');
const promise2 = Promise.resolve('Promise 2');

handleMultiplePromises(promise1, promise2)
  .then((values) => {
    console.log(values);
  });

4. Simple promise

Implement the function getStarted(), which returns a resolved promise after a certain delay. Example usage:

javascript

import signUpUser from './4-user-promise.js';

signUpUser('john.doe@example.com', 'password123')
  .then((user) => {
    console.log(user);
  })
  .catch((error) => {
    console.log(error);
  });

5. Reject the promises

Implement the function uploadPhoto() that returns a rejected promise with a custom error message. Example usage:

javascript

import uploadPhoto from './5-photo-reject.js';

uploadPhoto('photo.jpg')
  .then(() => {
    console.log('Photo uploaded');
  })
  .catch((error) => {
    console.log(error);
  });

6. Handle multiple promises

Implement the function handleProfileSignup(firstName, lastName, filename) that uses the signUpUser and uploadPhoto functions internally. It returns an array containing the resolved values of both promises. Example usage:

javascript

import handleProfileSignup from './6-final-user.js';

handleProfileSignup('John', 'Doe', 'john.jpg')
  .then((results) => {
    console.log(results);
  })
  .catch((error) => {
    console.log(error);
  });

7. Load balancer

Implement the function sendPaymentRequestToApi(endpoint, success, body) that returns a Promise using the fetch API to send a POST request to the input endpoint with the given body. The function simulates a network request and balances the load between multiple API endpoints by retrying failed requests with a different endpoint. Example usage:

javascript

import sendPaymentRequestToApi from './7-load_balancer.js';

const endpoint = 'http://api-load-balancer.com';
const success = true;
const body = JSON.stringify({ username: 'example' });

sendPaymentRequestToApi(endpoint, success, body)
  .then((response) => {
    console.log(response);
  })
  .catch((error) => {
    console.log(error);
  });

8. Throw error / try catch

Implement the function divideFunction(numerator, denominator) that divides two numbers and handles potential errors using try/catch. Example usage:

javascript

import divideFunction from './8-try.js';

try {
  console.log(divideFunction(10, 2));
  console.log(divideFunction(10, 0));
} catch (error) {
  console.log(error);
}

9. Throw an error

Implement the function guardrail(mathFunction) that wraps a given math function and handles potential errors using try/catch. Example usage:

javascript

import guardrail from './9-try.js';

const divide = (x, y) => {
  if (y === 0) {
    throw new Error('Cannot divide by 0');
  }
  return x / y;
};

const func = guardrail(divide);
console.log(func(4, 2));
console.log(func(4, 0));

10. Await / Async

Implement the function uploadPhoto() that simulates an asynchronous file upload process. It uses setTimeout to simulate a delay and returns a resolved promise after the specified delay. Example usage:

javascript

import uploadPhoto from './100-await.js';

async function handleProfilePictureUpload() {
  try {
    const result = await uploadPhoto();
    console.log(result);
  } catch (error) {
    console.log(error);
  }
}

handleProfilePictureUpload();


