### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
  in the controller we set flash[:whatever_type] = whatever_message
  and then in the view (or the application layout) we iterate thru flash.each and display each message with a content_tag

2. Where is cart information/temporary information usually stored?
  in a cookie

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  Storing info in the database means extra query calls on the database; keeping it client side makes it faster. We might want to persist the info if we want the information to exist from session to session

4. What is the purpose of the asset pipeline?
  provides a way to compress data for browser consumption

5. Why do we precompile our assets?
  Precompiling stuff translates things to more basic languages

6. What do each of the following tags do?
  the stylesheet one links our css files
  the javascript one I assume links our javascript files
  the image_tag displays images

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>>
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
    A readme should have info about what the project is and who it's for, as well as clear instructions about usage if needed.
    Benefits include people being informed about your project and informing your future self about the project

8. What are the top four accessibility issues that we as developers should be aware of?
  ????

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  That's a callback. We might find it in a controller, or in application controller

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
  scope :true, where(:active => true)


11. What is the difference between a scope and a class method?
  They're pretty similar, in my mind


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  cart["48"] = 4
  12b. How would you increase the quantity of item 29?  cart["29"] += 1
  12c. How would you find out how many items your user is thinking about purchasing?   cart.values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
  Polymorphism is about inheritance and subclasses and superclasses. I have no idea what duck-typing is - I'm pretty sure we haven't covered that. :( I think it has something to do with using methods in different places that are called the same thing but do different things?

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
    gsub(/[() -]/, {" " => ".", "-" => "."}) (I'm sure there's a better way to do this...)


### Self Assessment:
Choose One:
* I was able to answer a few questions independently, but relied heavily on outside resources
    I felt like there was a bunch of stuff we didn't cover - maybe I fell asleep?

Choose One:
* I feel overwhelmed by the content presented this week
