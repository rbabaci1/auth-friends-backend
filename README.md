# auth-friends-backend-server

## Project Description

* There is an API built that has authentication built into it. The API holds a list of friends and lets you add, edit, or remove friends from that list. 
* All of the API endpoints (except the login endpoint) are considered "protected", meaning you have to make the request with an authentication token in the header or the API will send back a `401` error. 
* Take your examples from the guided project and use them to build a more sophisticated application. Have fun!
* Once your server is up and running, the URL you'll be able to hit from within your app is 
`https://rabah-backend.herokuapp.com`. You will however need an authentication header on all the calls except the login call.
* Take a look at the endpoints that our API has to offer in `server.js`.

  * **[POST]** * to `/api/login`: returns a token to be added to the header of all other requests. Pass in the following credentials as the `body` of the request: `{ username: 'Lambda School', password: 'i<3Lambd4' }`
  * **[GET]** to `/api/friends`: returns the list of friends.
  * **[GET]** to `/api/friends/123`: returns the friend with the id passed as part of the URL (123 in example).
  * **[POST]** to `/api/friends`: creates a friend and return the new list of friends. Pass the friend as the `body` of the request (the second argument passed to `axios.post`).
  * **[PUT]** to `/api/friends/:id`: updates the friend using the `id` passed as part of the URL. Send the an object with the updated information as the `body` of the request (the second argument passed to `axios.put`).
  * **[DELETE]** to `/api/friends/123`: removes the friend using the `id` passed as part of the URL (123 in example).

## Initialize Project

* Run `npm install` inside the root directory of this project to install dependencies for the API server.
* Run `npm start` to start the API server.

**Adding New Friends**
* Create a form to collects data for a new friend.
* Make a POST request to add a friend to the database
* Each `friend` item that is in the `friends` array should have the following format:

```js
{
  id: 1
  name: 'Joe',
  age: 24,
  email: 'joe@lambdaschool.com',
}
```
