---
layout: post
title:      "Securing Passwords"
date:       2018-04-20 01:22:02 +0000
permalink:  securing_passwords
---


password
Password
Password1
@Password1
@PasswordPassword1
@Pa88word1Pa88word1!
@Pa88WOrd1Pa88WOrd1!
@P!a#8$8%W^O&r#d1@P!a#8$8%W^O&r#d1!


**...Passwords can be hard.**


Before I became a programmer, I could get SO angry with a website or app when it required me to create a difficult-to-guess password. Lately, however, I've realized how important passwords are. In fact, I've learned that securing passwords (and other user data) is one of the most quintessential jobs of a software engineer. And after creating a recent Sinatra application, I wanted to make note of one of the many ways that a programmer can secure the user's password. 

I recently created a web app called "Urban Wonder." It is a neat travel app written in Ruby on the Sinatra web framework. Please check it out (and watch the demo!) in my most recent blog post. 

While writing the code for Urban Wonder, it was clear that a user would need to create a password/username to access and store their personal data. After implementing this functionality, I wanted to ensure that the user's password data would not be stored blatantly in the app. In order to avoid being stolen, passwords would need to be encrypted before being stored in the database. To accomplish this, I would need to employ the Ruby gem, 'BCrypt.' 

I started this process by including BCrypt in the gem file. Then I added a 'password_digest' column in the users table and the 'has_secure_password' method in the User model. This particular method comes built into the BCrypt gem installation and encrypts a password by hashing, salting, and storing it inside the password_digest column. More simply, this means that the has_secure_password method throws random data into the user-generated password, mixes it around, and ultimately stores that information in the user's personal information vault so that only the exact same password entered in the proper place can unlock the rest of the data associated with a user.

In order to test my (hopefully) secure password, I placed a binding.pry in the post '/signup' view. I spun up a shotgun server, created a user in the browser, and a pry session began. When I entered @user, the terminal returned four attributes of my user class. It listed the primary key ID, the username, and email of the user properly, just as expected. But it did not list the password. Instead, it printed the following: 

"$2a$10$qhMEEnpSR7wqsGTIBGTGmOgGF5w7DDY0.YPRVCVkSy/6O0r1OWCEG"

Apparently, BCrypt and the has_secure_password did their job! I can't even find my password in this odd string of characters. After using this secure password method, I was also able to use the authenticate method inside of the post '/login' route to make sure that a user could login if the password entered into the login form matched the password originally created in the setup form.  

While doing this project, I learned that (in addition to being extremely important) securing passwords and other user data can also be very satisfying. There are a thousand new things to learn in the area of cryptography and it is gratifying to know that you are guarding sensitive information, promoting a better user experience, and creating a safe product all at once.
