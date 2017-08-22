## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

**1. List the five common HTTP verbs and what the purpose is of each verb.**

GET: request a resource.
POST: submit/create data.
PUT: Update/replace data.
DELETE: Delete resource.
HEAD: Same as GET, but only requests the header.

**2. What is Sinatra?**

A domain specific language to create websites with reduced effort.

**4. What is MVC?**

Model, Views, Controller.  It is a software architecture, primarily for creating GUIs.

**5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?**

In order to ensure compatability with the HTTP standard requests and making the code easier to read.

**6. What types of variables are accessible in our view templates without explicitly passing them?**

Instance variables.

**7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?**

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

**8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?**

```ruby
get '/horses' do
  @name = 'Mr. Ed'
  erb :index
end
```

**9. What's the purpose of ERB?**

An HTML file with ruby code included in it. The DSL will evaluate the form in order to dynamically create a HTML file.

**10. Why do I need a development AND test database?**

The test database is created for testing your system, and is often a fixture. The development database is more reflective of your actual production database and allows for more flexibility during development.

**11. What's responsive design?**

Designing web contact that will respond to adjust depending on how the user is consuming the content, allowing it to be adjusted from desktop viewing to phone viewing without losing content.

**12. What is CRUD and why is it important?**

Create, Read, Update, Delete. It is the basis for utilzing databases, the user needs to be able to view, modify, and delete data as necessary.

**13. What does HTTP stand for?**

Hypertext Transfer Protocol

**14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?**

_<%= INSERTCODE %>_ Code is evaluated and placed in the HTML file.
_<% INSERTCODE %>_ Code is executed.


**15. What's an ORM?**

Object Resource Manager.

**16. What's the most commonly used ORM in ruby (Sinatra & Rails)?**

ActiveRecord

**17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.**

_get '/restaurants' do_ Allows user to request restaurants page.

_get '/restaurants/new' do_ Directs user to restaurant create page.

_get '/restaurants:id/edit' do_ Allows user to edit restaurant entry.

_get '/restaurants:id' do_ Directs user to specified restaurant.

_post '/restaurants' do_ Pushes the newly created restaurant to the database.

_put '/restaurants' do_ Allow for the updating of restaurants.

_delete '/restaurants:id' do_ Removes the restaurant, specifid by id, from the database.

**18. What's a migration?**

A set of instructions used to create a database.


**19. When you create a migration, does it automatically modify your database?**

No, not until you modify the migration file to include the modifications you want present and run migrate on the DB.


**20. How does a model relate to a database?**

The model is used for determining the relationships between objects in the database and actually querying the database.

**21. What's the difference between agile workflow and waterfall method?**

The waterfall method is just a single sprint between planning and development, the agile method breaks the same process up into smaller pieces that follow the same format.

**22. What is the difference between `#new` and `#create`?**

New makes the object, but does not save it. Create makes the object and saves it at the same time.
