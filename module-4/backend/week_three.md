## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. At a high level, what is Node?

A runtime for utilizing JavaScript for server side applications.

2. What is Express? What is Express similar to in the Ruby world?

A web application framework for JavaScript. It is similar to Sinatra for Ruby.

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

A JavaScript script in the root directory, in the case of the last project the `server.js` file. In that file the routes are created as follows utilizing Express.js:

```Javascript
const express = require('express')
const app = express()

app.get('/api/v1/model/:id', jsController.action)

```

4. What do we use Knex for?

To interact with PostgreSQL with JavaScript, similarly to how ActiveRecord works in Ruby.

5. How **could** you organize your code to follow the MVC design pattern in your Quantified Self project?

Ours was organized relatively similarly to the MVC model. Data formatting and processing was handled by models, the `server.js` file functioned similarly to how a controller would, and views were separated.

6. How do you execute raw SQL in node?

By utilizing knex to perform a `raw` sql function on the data itself.

```JavaScript
database.raw(
    'INSERT INTO foods_meals (food_id, meal_id) VALUES (?, ?)',
    [food_id, meal_id])
```

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

One of the advantages is that neither is dependent upon the other, such that at any time you can swap out either the back or front end without much additional work, allowing for a much more modular design. Some of the disadvantages are that it increases the complexity of each and you have to work around various communication issues.

#### Review  

8. Describe DNS.

Domain Name Server, the internet services that translates domain names (ala, www.google.com) into routable IP addresses.

9. What does writing clean code mean to you?

Code that is readable, broken into smaller more manageable pieces, and is not repetitive. Also, logic is well organized into sensible parts.

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality? Hint: think about what tables you would need in the database, how those records would relate to each other, and good OOP.

Hotel: Has many rooms, has many customers.
  ID, name, address, # of rooms
Room: Belongs to hotel, belongs to customers
  ID, room_number, type
Customer: has many rooms.
  ID, name, address, phone_number
