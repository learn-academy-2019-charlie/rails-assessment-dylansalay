# Rails Assessments

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

### 1. What are some advantages of using Ruby on Rails?
  Ruby on Rails is very readable.
  It is a popular language so there is good documentation and lots of resources available.
  It is an open-source framework.
  It follows the Model-View-Controller architecure.
  There are gems available for a variety of different functionality.  
  

### 2. How does Ruby on Rails use the Model View Controller (MVC) framework?
    Rails stores the code for each of the MVC elements in separate directories. Active record is the module that handles all of the logic and business communication, thus playing the role of Model in our MVC framework. When a user makes a request online, it is the job of the Controller to take in the request, control traffic, and facilitate communication between the Model and the View. Lastly, the View is responsible for handling the presentation of the page to the user.

### 3. Using the information given, complete the steps for creating a new view in a rails app by filling in the blanks:

  1. Create a route: 
  
  code: 
  ```
  get '/about' => 'statics#about' 
  ```
  file: config/routes
  
  2. Create the controller
  
  code: 
  ```
  class StaticsController < ApplicationController
  
  def about 
    @name = name
  end
  ```
  
  file: statics_controller.rb
  
  3. Create the View
  
  code: 
  
  ```
  <div>This is the About page!</div>
  ```
  
  file: about.html.erb
  
  
### 4. Look at these sets of Rails routes, they are an example of which principle/term that we touched on briefly in class? Find the term, and explain why it is important.

```
/users/       method="GET"     # :controller => 'users', :action => 'index'
/users/1      method="GET"     # :controller => 'users', :action => 'show'
/users/new    method="GET"     # :controller => 'users', :action => 'new'
/users/       method="POST"    # :controller => 'users', :action => 'create'
/users/1/edit method="GET"     # :controller => 'users', :action => 'edit'
/users/1      method="PUT"     # :controller => 'users', :action => 'update'
/users/1      method="DELETE"  # :controller => 'users', :action => 'destroy'
```

C - Create
R - Read
U - Update
D - Delete

Models should be able to perform the four CRUD functions. The concept of CRUD is important because it provides are framework for building fully functioning models. 


### 5. What is the public folder used for in Rails?

The public folder contains HTTP templates for some of the common HTTP errors such as 404, 422 and 500. 

Per the rails documentation - "The only folder seen by the world as-is. Contains static files and compiled assets."

### 6. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

get "/game/:guess" => "main#game"

### 7. What are cookies for? How do they work? What is the difference between a session and a cookie?

Both cookies and sessions allow us to store data between page refreshes and redirects. The primary difference between the two is that a cookie is a bit of data stored by the browser that is sent to the server with every request while a session is a collection of data stored on the server and associated with a given user.

### 8. In an html form, what does the "action" attribute tell you about the form?  How do you designate the HTTP verb for the form?

The action attribute specifies where the browser should send the form data. The http verb is designated via the method attribute. 


### 9. Why would you use an instance variable in a rails controller?

Instance variables are used within methods in the rails controller to pass static information to the view. 

### 10. Name two rails generator commands and what files they create:

rails generate model is used to generate the model within the rails application, and any columns:datatypes within that model.
rails generate controller is used to create the controller file, a view file, a functional test file, and a javascript file. 

### 11. Rails has a great community and lots of free tutorials to help you learn. Here is a list of some tutorials to choose from, choose one, do it, and then report back here at least one thing you learned. You can also use a different resource if you find one that you like better. 

- https://www.tutorialspoint.com/ruby-on-rails/index.htm
- http://railsforzombies.org
- http://guides.rubyonrails.org/getting_started.html


The link_to method is one of Rails' built-in view helpers. It creates a hyperlink based on text to display and where to go.

ex.  <%= link_to 'New article', controller: 'articles' %> 

The link is called "New article" and the route is to the articles controller. 
