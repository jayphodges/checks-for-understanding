## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

**1. What is the entry at the command line to create a new rails app?**

rails new <project_name> --T --database=postgresql --skip-spring --skip-turbolinks

**2. What do Models generally inherit from in rails?**
```ruby
ApplicationRecord
```
**3. What do Controllers generally inherit from in a rails project?**
```ruby
ApplicationController
```
**4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?**
```ruby
resources :horses, only [:show]
```
**5. What rake task is useful when looking at routes, and what information does it give you?**

rake routes. It gives you a list of the available routes with their URI, action, and prefix.

**6. What is an example of a route helper? When would you use them?**
```ruby
horses_path(horses)
```
Anytime you are routing through rails, it is a simplified nomenclature for the path.

**7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?**



**8. What are strong params and why are the necessary?**

Prevents data you do not want from being passed into your controller.


**9. What role does `form_for` play in helping us create our forms?**

It defines the model you are creating the form for, allowing you to call upon the attributes of the model in order to create the form.

**10. How does `form_for` know where to submit the user's input?**

The controller's create and edit paths.

**11. Create a form using a `form_for` helper to create a new `Horse`. **
```ruby
<%= form_for(@horse) do |f| %>

<%= f.label :name %>
<%= f.text_field :name %>

<%= f.label :age %>
<%= f.text_field :age %>

<%= f.label :owner %>
<%= f.text_field :owner %>

<%= f.submit %>
```

**12. Why do we want to validate our models?**

To ensure they work as we expect them to.
