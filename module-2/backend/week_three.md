## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?

rails new 'folder_name' -T -d="postgresql"

2. What do Models generally inherit from in rails?

ApplicationRecord < ActiveRecord

3. What do Controllers generally inherit from in a rails project?

ApplicationController < ActionController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

in config/routes.rb -add- resources :horses, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

rake routes -- allows you to see the route helper, uri path, and controller action

6. What is an example of a route helper? When would you use them?

horses_path - takes you to the index of horses. Use the path whenever possible - test/view/controller

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

a path helper is a direct connection to the route, whereas a url is prone to changing

8. What are strong params and why are they necessary?

strong params are when you are filtering the params for an argument. It restricts what can be used for security purposes

9. What role does `form_for` play in helping us create our forms?

form_for is rails customizable setup for a form and can refer to any params needed to be submitted(passed)

10. How does `form_for` know where to submit the user's input?

depending on the name/action of the view, it will accommodate the action needed.

11. Create a form using a `form_for` helper to create a new `Horse`.

<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.label :breed %>
  <%= f.text_field :breed %>
  <%= f.label :color %>
  <%= f.text_field :color %>
  <%= f.submit %>
<% end %>

12. Why do we want to validate our models?

to make sure we can only create objects of those models with required attributes,
 and nothing less.

13. What are the steps of the DNS lookup?

browser TO operating system TO internet service provider TO root server TO top
level domain server TO authoritative name server ---- Then back down the chain.

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>`

   within("#personal-info") do
    expect(page).to have_content(@person.name)
   end
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?

horse = Horse.new
horse.move.prance

16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  

furniture[:table][:height]
furniture[:purchased]

17. What is inheritance?

receiving the properties of existing objects

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
### * I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
### * I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
