req.user = await User.findOne({ \_id }).select("\_id");

This line search for the id of the logged in user and return that id to match with the ids of the tours and the todo tasks.

userSchema.statics.signup()/userSchema.statics.login()
Is a static function that gets called in userController in order to store the details of an user who is signing up/logging in. This is done rather than writing the logic of sign up/log in directly in userController.

They are used to make the code in the controller cleaner and easily readable

Pros:- reusability, can be accessed globally within scope of the class,
Con:- function can not access instance variables or methods, limit in flexibility, harder in testing

Alternate approach:- writting the logic in userController.
