# ![Build and Run server.js](../assets/hero-build-and-run-serverjs.png)

In this lesson, we’ll create our **main entry point**, set up an **Express server**, and render our first **EJS view**.

## Step 1: Install the Express Module

Before we begin building our server, let's use `npm` to install the Express module in this project:

```bash
npm i express
```

> 📚 Note that `i` is a shortcut for `install` and npm is short for "node package manager"

Now that we've done this, the Express framework is available for us to use when building our application. Without this step, if we were to try to run our server code, we would receive an error since our app would be be trying to import a node module that we haven't installed yet.

Now that `express` is installed, let's write the basic code needed to create our server.

## Basic Structure of Express App

Here is a helpful outline of what a typical Express app does - let’s put this code right in our `server.js` file:

```js
// We begin by loading Express
const express = require('express')

// We create an instance of Express
const app = express()

app.listen(3000, () => {
  console.log('Listening on port 3000')
})
```

> 📚 The `server.js` file is typically the main entry point and configuration file for setting up an Express web server.

## Run the Server

Let's test our work by running our server. Run the following in your terminal:

```bash
nodemon
```

Our server should be up and running and you should see _`Listening on port 3000`_ logged to your terminal.

---

<div align="center">

### Next Up 👉

[**Use Mongoose to Connect to MongoDB**](./use-mongoose-to-connect-to-mongodb.md)

</div>

---
