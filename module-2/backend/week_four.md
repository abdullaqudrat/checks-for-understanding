## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?

It is a way for the website to designate identity to the client so it can pull information from the database about the client.

2. What’s the difference between a session and a cookie?

  A session is a way to connect the client to the websites memory of that client. A session is often stored in the database. A client's cookie will be carried its browser like an ID/rewards card in a wallet for that website.

3. What’s a flash and when do you want to use flashes?

  A flash is a type of notice/message that is typically used when the user is submitting something to the website.

4. Why do people say “HTTP is stateless”?

  HTTP is stateless because it doesn't remember or distinguish from one request to another. Using cookies and sessions is a way to mimic state in an otherwise stateless interaction.

5. What’s authentication? Explain.

  Authentication is a way to distinguish a user from a visitor. It typically requires a username and password to authenticate a user with the user's account in the database. It can save information and authorize specific user access for that user.

6. What’s the difference between authentication and authorization?

  Authorization is a way to setup compartmentalized framework so that specific user access can be viewed. Authentication can be a part of authorization. Authorization may not necessarily involve authentication.

7. What’s a before filter?

  The "before filter" requests that before anything else is defined, do the actions in specified

8. How do we keep track of a user once they’ve logged in?

  Once the user has logged in, we can keep track of the user by setting the user to a session, and it will remain set to the user, until the user logs out, where the session will be unset from the user.

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

  You want to namespace a resource for organizational/compartmentalizing purposes. You want to nest a resource when you have two objects that have a one to many relationship.

10. At a high level, what tools can you use to implement authorization? How would you use them?

  enums - sets role for user to specify what type of access they have
  before filters - to verify access based on role of user
  helper methods - sets the current user

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

  Enums can specify certain roles for a user, where a role is set as an attribute in for user in the database. Enum is an array declared in the user model.

12. What are some strategies you can use to keep your views DRY?

  Using partials to render in your page. Setting instance variables in your controllers to refer to in your view

### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]

holiday.map do |hash|
  hash[:holiday][:name]
end.sort
```  
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

  number.gsub(/[^\d\.-]/,'').to_i


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
### * I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
### * I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
