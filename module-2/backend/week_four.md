### Questions

* **What is a cookie?**

  An information containing file downloaded by the browser by websites, in order to retain information.

* **What’s the difference between a session and a cookie?**

  Sessions are supposed to delete themselves when you close the browser.

* **What’s a flash and when do you want to use flashes?**

  A way of passing temporary messages, such as alerts to the browser.

* **Why do people say “HTTP is stateless”?**

  Because it does not retain information between sessions.

* **What’s authentication? Explain.**

  A process that verifies the identity of someone.

* **What’s the difference between authentication and authorization?**

  Authentication tells you the user is who they say they are, authorization is controlling what each user is allowed to access.

* **What’s a before filter?**

  Something that runs before each action in a controller.

* **How do we keep track of a user once they’ve logged in?**

  By saving their information in a session.

* **When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?**

  In order to allow model specific access to resources, such as having to browse sub-categories, or allowing user and admin specific views.

* **At a high level, what tools can you use to implement authorization? How would you use them?**

  You can use `before_action` in the controllers, as well as user specific actions in the views, and redirects for certain users.

* **What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?**

  An enum maps strings to integers in Ruby. So as opposed to having to hold strings such as "default" and "admin", you can use a enum on an integer in your database. It is declared in the model itself, as such: `enum role: [:default, :admin]`.

* **What are some strategies you can use to keep your views DRY?**

  By creating forms for any content that is going to be reused from page to page.
