#Secure Passwords and the User Model

1. Could you create a user without an email? How do you know?
No, because there is a authenticate on email set to true meaning email has to be present. 

2. How would you call the User model's password getter method (is it an instance method or a class method)?
The user model's password getter method is a class method, since it is in a self block. 

3. Is the User model's password= an instance method or a class method? What is it using BCrypt for?
The user model's password= is a class method because we need a user to call the password. BCrypt is to add encryption to the user generated password. 

4. Is the User model's authenticate an instance method or a class method? What does it use BCrypt for? What does it return if passwords match? 
The User model's authenticate is a class method because it is in a self block. BCrypt is used for encryption, if the password match it returns the secure password. 

5. How would you call the User model's self.confirm method (is it an instance method or a class method)? What does it do?
The User Model's self.confirm method is an instance method because it calls upon the mail and password params. 

6. Which User model method interacts with the database?
The User.find_by_email method interacts with the database. 

#Login/Logout with Sessions 

1. What object does Rails give us to access session information? What kind of object is it?
Rails will create a new seession with a has of values and a session id. 

2. Why do we have a SessionsController?
Seession controller dictates login and logout to generate new sessions for users. 

3. What does the sessions#new controller action do?
Session#new validifies the user to their session. 

4. The sessions#create controller action controls login. What does sessions#create do if login succeeds? What if it fails?
If login is successful, generates a new session. If it fails, redirects to root path. 

5. What does sessions#destroy do (signup, login, or logout)?
The session will be terminated. 

6. What route(s) would we have to add if we want users to be able to edit their information?
To edit their information, need to add :edit route. 


#Current User with Helper Method 

1. Why would we want to keep track of the currently logged in user?
To keep track of resources and legitimate users to prevent hackers using duplicate logins. 

2. What is the current_user helper method in app/controllers/application_controller.rb doing?
Keep track of the currently logged in users base on their user id and their session. 