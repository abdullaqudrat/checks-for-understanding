### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?

To activate a flash message, it needs to be called and expressed in the controller. To display, the flash needs be called in the application.html.erb file in layout folder.

2. Where is cart information/temporary information usually stored?

Its usually stored in session or cookie.

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?

If you store the cart in the database, it will stay and take up space in database for purchases that weren't intended. That info may persist if a site wants to store data on what products the customer may be interested in purchasing in the future.

4. What is the purpose of the asset pipeline?

The purpose of the asset pipeline is to load the app faster on browser. It saves the browser from recurring requests render a site and it combines all the files of that asset and clears out white spaces and comments.

5. Why do we precompile our assets?

Precompiling assets allows for faster loading of those specific assets

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %> This allows you to retrieve a CSS file compiled by the asset pipeline
<%= javascript_include_tag "application" %> This allows you to retrieve a Javascript file compiled by the asset pipeline
<%= image_tag "rails.png" %> This allows you to retrieve an image file compiled by the asset pipeline
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

Describe what your project is by a well written intro paragraph.
How to use the project by supplying clear/thorough instructions, including: pictures/gifs, and any references to other libraries/dependancies being used.
Document the installation process clearly and simply, with code and pics.
State the requirements, and if any features still in progress.

8. What are the top four accessibility issues that we as developers should be aware of?
 Visual
 Motor
 Hearing
 Cognitive

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

Its and example of a callback. A callback is implemented in the controller.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
class User < ApplicationRecord
  scope :active, -> { where(active: 'true') }
end

11. What is the difference between a scope and a class method?

A scope will always return an AR relation object even if the conditional is false, where as a simple class method will return a nil and will cause a no method error when chaining classes.

### Review Questions:  
12. Given the following hash:  

```ruby
contents = {cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  

  contents[:cart]['48'] = 4

  12b. How would you increase the quantity of item 29?  

  contents[:cart]['48'] += 25

  12c. How would you find out how many items your user is thinking about purchasing?

  contents[:cart].size

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?

Allows you to call the same method on 2 different classes and get 2 different results. If the object has the method, then it is the correct method for that object. 

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  

string.gsub(/[()]/,'').gsub(/[' '\-]/,'.')

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
