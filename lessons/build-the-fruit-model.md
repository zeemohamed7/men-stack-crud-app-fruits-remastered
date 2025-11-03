# ![Build the Fruit Model](../assets/hero-build-the-fruit-model.png)

In this lesson, students will be able to define and export a Mongoose model.

## Creating a Model

As we progress with our application, the next essential step is to create a schema and model for our fruits. This process will define how our fruit data is structured and stored in the database. By establishing a clear schema, we ensure consistency and reliability in the data we handle. Additionally, the model created from this schema will serve as the main interface for our application to interact with the MongoDB database, allowing us to perform CRUD operations on fruit data. Let's dive into creating our first Mongoose schema and model for the fruits in our application.

## Create the model file `Fruit.js`

Let's create a directory that will hold the file for our fruit model `Fruit.js`:

```bash
mkdir models
touch models/Fruit.js
```

Creating a dedicated directory for a single file may seem unnecessary, but it's actually a strategic approach in software development. This practice is beneficial for future scalability. For instance, if you later decide to add more models to your application, having a designated `models` directory allows for clear organization, with each model having its own separate file. This makes your codebase more structured and manageable.

Here's how we'll structure our `Fruit.js` file:

- **Create the schema:** We'll begin by defining the schema for a `Fruit`. This schema is like a blueprint, describing the properties and characteristics of what a `Fruit` object should include.

- **Link the schema to a Model:** Next, we'll create a model from our schema. This model is essentially a representation of a MongoDB collection. By linking our schema to this model, we connect the defined structure of our `Fruit` data to the corresponding collection in the database.

- **Export the Model:** Finally, we need to make sure our model is available for use elsewhere in our application. We'll do this by exporting the model from the Fruit.js file.

You should name models and model files singularly. For example, `Fruit.js` instead of `Fruits.js`. This is because a model is a singular representation of the data you are storing.

## Create the fruits schema

Before we define our model, we must first import the mongoose library into our `Fruit.js` file:

```javascript
// models/Fruit.js

const mongoose = require('mongoose')
```

Now let's define the schema for our `Fruit` model. A schema in Mongoose is a way to structure the data in our database. It's essentially a JavaScript object where each key represents a property of our data. The value assigned to each key specifies the type of data we expect for that property and can also include certain constraints or rules.

For our `Fruit` model, we want to keep it simple. We'll have two properties: `name`, which will be a string, and `isReadyToEat`, which will be a boolean indicating whether the fruit is ready to be eaten.

Here's what this would look like in our `Fruit.js` file:

```javascript
// models/Fruit.js

const mongoose = require('mongoose')

const fruitSchema = new mongoose.Schema({
  name: String,
  isReadyToEat: Boolean
})
```

## Register the model

After defining our schema, the next step is to inform Mongoose about the collection in MongoDB that will use this schema for its documents. We achieve this by creating a model. A model in Mongoose serves as a constructor for creating new documents, and it also enforces the structure defined in the schema.

To create a model, we use the `mongoose.model` method. This method takes two arguments: the `name` of the model and the `schema` to apply to that model.

Here's how we define the model for our `fruit` schema:

```javascript
// models/Fruit.js

const mongoose = require('mongoose')

const fruitSchema = new mongoose.Schema({
  name: String,
  isReadyToEat: Boolean
})

const Fruit = mongoose.model('Fruit', fruitSchema) // create model
```

> Note: There is a convention to use a capital letter for database model names, so name your model `Fruit`, as opposed to `fruit`.

## Export the model from the `Fruit.js` file

Next, we want to export the `Fruit` model we just created, so that the rest of our application has access to it.

The `Fruit` model is what we will use to perform CRUD on the collection.

```javascript
// models/Fruit.js

module.exports = Fruit
```

> ### ✅ Checkpoint

Your `Fruit.js` should look like this:

```javascript
// models/Fruit.js

const mongoose = require('mongoose')

const fruitSchema = new mongoose.Schema({
  name: String,
  isReadyToEat: Boolean
})

const Fruit = mongoose.model('Fruit', fruitSchema)

module.exports = Fruit
```

---

<div align="center">

### Next Up 👉

[**Build the Fruits Index Page**](./build-the-fruits-index-page.md)

</div>

---
