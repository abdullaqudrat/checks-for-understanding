## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.

  GET - read
  PUT - updates
  PATCH - updates
  POST - create
  DELETE - destroy


2. What is Sinatra?

Its a web application framework

3. What is MVC?

Model - in charge of interacting with database
View - in charge of displaying page with info from database
Controller - in charge traffic between the model and view, to provide http requests

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

It is a model that is RESTful

5. What types of variables are accessible in our view templates without explicitly passing them?

partials i.e. params

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

@name = 'Mr. Ed'

8. What's the purpose of ERB?

to implement ruby code into html so we can display info

9. Why do I need a development AND test database?

So we can test our MVC without having to seed a database, like we would in development

10. What is CRUD and why is it important?

Create, Read, Update, Destroy.

It is the basis of functionality when working with a database

11. What does HTTP stand for?

Hyper Text Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

<%= person.name %> - this echoes(prints)
<% person.name %> - this does not echo

13. What's an ORM? What does it do?

Object Relational Mappers

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?

ActiveRecord
DataMapper
Sequel

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

get '/restaurants' - gets index of restaurants
get '/restaurants/new' - gets new restaurant form
get '/restaurants/:name' - gets specific restaurant
get '/restaurants/:name/edit' - gets edit for specific restaurant
post '/restaurants' - creates new restaurant
put '/restaurants/:name' - updates specific restaurant
delete '/restaurants/:name' - deletes specific restaurant

16. What's a migration?

creates table in database

17. When you create a migration, does it automatically modify your database?

no, it allows you to create/modify a table with attributes, then you can migrate

18. How does a model relate to a database?

thru the migration file

19. What is the difference between `#new` and `#create`?

new makes an object, but create saves it to the database

20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    `
SELECT * FROM animals;

21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?

SELECT * FROM animals WHERE number_of_legs=4

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

CSV.foreach('films.csv', headers: true, header_converters: :symbol) do |film|
  Film.create(id:           film[:id],
              title:        film[:title],
              description:  film[:description]
              )

23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```

How would I add 'granola bar' to things you should have when hiking?

activities[:hiking][:supplies].push('granola bar')

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.

Abstraction - working with something we know how to use without knowing how it works internally
Encapsulation - hiding of data implementation by restricting access to accessors and
Inheritance - It allows a class to "inherit" of another, more general class
Polymorphism - objects of different types can be accessed through the same interface.

### Self Assessment:
Choose One: (erase the others)
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
##* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
##* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
