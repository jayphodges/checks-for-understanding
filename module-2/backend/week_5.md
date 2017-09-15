**1. How do we make flash messages display on a page?**

By creating a flash message in the controller as well as creating a way for it to render on the page.

```ruby
flash[:notice] = "This #{@message.name} will self distruct in #{@bomb.fuse_duration}!"
```

```ruby
<% flash.each do |type, message| %>
<%= content_tag :div, sanitize(message), class: type %>
<% end %>        >
```

**2. Where is cart information/temporary information usually stored?**

In the session.

**3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?**

The advantage to a session is that it resets when the customer closes their browser and is automatically encrypted.

**4. What is the purpose of the asset pipeline?**

Converting all your styles and assets into a format that will load more quickly, and ensuring that everything is converted into a language that the browser will understand.

**5. Why do we precompile our assets?**

To improve load times and reduce bandwidth.

**6. What do each of the following tags do?**


```<%= stylesheet_link_tag "application" %>``` Tells Rails to create the HTML link to the CSS stylesheet.


```<%= javascript_include_tag "application" %>``` Tells Rails to create the HTML link to your javascript asset.


```<%= image_tag "rails.png" %>```  Tells Rails to create the HTML to link to an image in your assets.

**7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?**

What your project does, how to install it, how to use it, are there any issues, how do you contribute, how do you contact the developer.

The benefit of creating a great readme is the amount of time it saves in the future. Making the information available ensures that nobody has to go searching for how to use the program, and may help yourself in the future if you have to go back to the project.

**8. What are the top four accessibility issues that we as developers should be aware of?**

* Visual
* Cognitive
* Mobility
* Hearing

**9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?**

It is an example of a callback, and we would find it in the model ensuring the action is taken before a create.

**10. Given the following object, how would we create a scope for all users who are active?**

```ruby
User.create(name: "Happy", active: true)
```

```ruby
scope :active, -> { where(active: true) }
```

**11. What is the difference between a scope and a class method?**

A scope is essentially a class method explicitly for retrieving and querying ActiveRecord objects.
