## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  GET, POST, PUT, PATCH, DELETE

2. What is Sinatra?
  Framework for writing Web Applications, sort of like Rails

3. What is MVC?
  Model Views Controllers

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  So other programmers can read our stuff?

5. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template? @count = 1

  ```ruby
  get '/horses' do
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  name = 'Mr. Ed'

8. What's the purpose of ERB?
  Write ruby code in HTML

9. Why do I need a development AND test database?
  So you don't have to use the entire huge database for each test. Also, so you can delete and edit things in tests.

10. What is CRUD and why is it important?
  Create, Read, Update, Destroy - Super important database functions

11. What does HTTP stand for?
  Hypertext Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <% %> and <%= %> - the one with the equals prints to the screen

13. What's an ORM? What does it do?
  Object Relational Mappers. It makes the database easier to interact with through Ruby.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  1. GET /restaurants
  2. GET /restaurants/new
  3. POST /restaurants
  4. GET /restaurants/:id
  5. GET /restaurants/:id/edit
  6. PUT /restaurants/:id
  7. DELETE /restaurants


16. What's a migration?
  A migration is what you do when you want to make changes to the schema

17. When you create a migration, does it automatically modify your database?
  No, you have to then migrate

18. How does a model relate to a database?

19. What is the difference between `#new` and `#create`?
  create does both new and save


### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

21. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  1. Encapsulation - keeping fields within a class private
  2. Abstraction - keeping underlying code secret from other code
  3. Inheritance - sharing attributes of other classes
  4. Polymorphism - a particular thing can mean more than one thing

### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
