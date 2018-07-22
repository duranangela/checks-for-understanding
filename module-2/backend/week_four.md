## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  A cookie is info stored on a client's computer

2. What’s the difference between a session and a cookie?
  A cookie is stored client-side, a session is server-side

3. What’s a flash and when do you want to use flashes?
  A flash is a message that happens after certain actions. You want to use them anytime you need to alert the user to that action or if you want confirmation about an action.

4. Why do people say “HTTP is stateless”?
  HTTP by itself doesn't retain information from one web interaction to the next

5. What’s authentication? Explain.
  Authentication is the whole process of logging in a registered user, or authenticating a user with a password and/or other credentials.

6. What’s the difference between authentication and authorization?
  Authentication is making sure a user is who they say they are, authorization is about what level of access that user has.

7. What’s a before filter?
  An event that we want to run before certain actions

8. How do we keep track of a user once they’ve logged in?
  We start a session, and that session persists while they're logged in

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  You namespace a resource when it will only be used by a certain level of authorization, you use a nested resource to attach one resource to another.

10. At a high level, what tools can you use to implement authorization? How would you use them?
  You use bcrypt to help with passwords, use enums to set roles, use namespacing to define admin actions

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  Enums make user roles (or anything probably?) a hash with number keys and role values. Yo have to have integers in the table. Enums are declared in the model.

12. What are some strategies you can use to keep your views DRY?
  Use render to show forms, use application layout to show the nav bar and flash messages


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
sorted = array.map do |index|
  (index[:holiday][:name])
end
puts sorted.sort


14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
  scan(/[.0-9]/).join().to_i

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
