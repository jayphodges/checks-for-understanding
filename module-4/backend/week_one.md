## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. **What's the most useful thing you learned from completing the intermission week work?**

Just the overall basics of JavaScript. I had previously somewhat resisted it, for example choosing to work with python for my mod 3 personal project, but I'm finally starting to enjoy it at least.

2. **What are some tools to help debug JavaScript code?**

Chrome console/ NodeJS developer tools, pryjs, firebug. In theory WebStorm but I can't for the life of me get much other than the chrome console working.

3. **What are some tools you need in order to unit test your JavaScript?**

Mocha and chai, or any of the other testing suites for JS.

4. **What is the syntax for invoking a function? Give an example.**

```JavaScript
doubleNumber(5);
> 10
```

5. **What's `this` in JavaScript?**

It references the closest relative object, be it a function or the DOM. It is contextual.

6. **What is Webpack and why is it useful?**

It prepares all of your assets for deployment by splitting them into more reasonable pieces, or modules; which can then be loaded on demand speeding content delivery.

7. **When/why do you want to use event delegation?**

Because it allows you to have an event listener on an element higher in the hierarchy allowing you to add children elements without having to create additional listeners.

8. **What's `npm` and what do we use it for?**

A package manager for JavaScript, specifically NodeJS, which allows you to manage your JS packages similarly to how you can manage Ruby Gems with `gem`. I would assume it stands for Node Package Manager, but annoyingly I can't seem to find it defined on the internet, so clearly it's one of those developer things where they pretend NPM isn't an acronym in order to give English majors a headache.

#### Review  
9. **What's the MVC design pattern? Describe each part of MVC.**

It is a design pattern used primarily for developing user interface focused products.

Models: Manages, stores, and formats data.
Views: Anything presented to the user.
Controllers: Defines logic and routing for the program.

10. **What are a few ways to optimize a Rails application?**

Background workers, cacheing, and database optimization.

11. **What's a background worker? When would we want to use a background worker?**

Code that is executed independently allowing you to move some processes away from your user interface in order to increases performance.
