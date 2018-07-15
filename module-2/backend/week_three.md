## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  rails new <project name> -T -d="postgresql" --skip-turbolinks --skip-spring

2. What do Models generally inherit from in rails?
  ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
  ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  resources :horses, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?
  rake routes or rails routes - tells you what restful paths are available

6. What is an example of a route helper? When would you use them?
  for example, horses_path instead of /horses for the index page. You want to use them all the time.

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?


8. What are strong params and why are they necessary?
  Strong params define what attributes are allowed and necessary for updates - they provide a layer of security so users don't 'accidentally' mess up sensitive info.

9. What role does `form_for` play in helping us create our forms?
  It defines what objects the form is for

10. How does `form_for` know where to submit the user's input?
  It's magically preset by the action in the controller

11. Create a form using a `form_for` helper to create a new `Horse`.
  <% form_for @horses do |f| %>
    <%= f.label :name %>
    <%= f.text_field :name %>
    <%= f.label :breed %>
    <%= f.text_field :breed %>
    <%= f.submit %>
  <% end %>

12. Why do we want to validate our models?
  to make sure all the attributes that are necessary are present

13. What are the steps of the DNS lookup?
  1. request goes to the dns resolver
  2. goes to the root name server
  3. goes back to dns resolver
  4. goes to top level domain server
  5. goes back to dns resolver
  6. goes to authoritative name server
  7. goes back to dns resolver
  8. goes back to client


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  def move
    prance
  end

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
  to return true you have to put both table and height in brackets, like so:
    furniture[table][height]
  as opposed to just putting furniture[purchased]


16. What is inheritance?
  When one class automatically gets the attributes of another class

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
