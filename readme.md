# User-Based Movie Collection Program

# General Rundown:

- Your program should allow a user to "log in" by giving their name,
  add to their movie collection, delete, update a movie, view all of a user's movies. If the user doesn't already have info being stored, then when they type their name in you should add them to the variable storing all of your users' info. Your program should allow the user to "log out" and another user "log in" without having to restart the program. This is likely not going to be easy for most of ya, through the fire and flames...we carry on.

# 3 Ways To Practice:

I am requiring you to use a certain variable that holds all of your users' data, depending on which module you want to practice it will be different. So that it makes your functionality different. Each movie should have AT LEAST: a name, and a director's name. You can add more if you want.

    # IF YOU'RE ON M3 you'll be using lists and tuples. Your variable containing the info of all users should be in the exact format of this example:

      all_users_info = [["Logan", [("Movie A", "Director A")]], ["Spencer", [("Movie B", "Director B")]]]

        Each user in the list is a list with 2 indexes, first index should be their name and second should be their movie collection which is a list of tuples, each movie is a tuple.

    =================================================================

    # IF YOU'RE ON M4 you'll be using a dictionary, lists, and tuples. Your variable will be in this exact format:

      all_users_info = {"Logan": [("Movie A", "Director A"), ("Movie B", "Director B")]}

      Your variable is a dictionary where the keys are the user's name and the value is a list of tuples, each movie is a tuple.

    =================================================================

    # IF YOU'RE ON M5 do the same as M4 except I expect AT LEAST 5 functions to be written, input helpers\validation functions don't count ;)


    =================================================================


    # IF YOU'RE ON M6 you'll be using a dicionary where the keys are the users' name and the value is a dataclass instantiation of their info.
    You should now require the use of a password to login/create a user.
    Users and movies should be a dataclass.

    Your variable will look like this:

      all_users_info = {"Logan": User("Logan Floyd", "D!4boLiCAl", [Movie("Movie A", "Director A"), Movie("Movie B", "Director B")])}

    ## MOVIE DATACLASS:

        @dataclass
        class Movie:
          movieName: str
          directedBy: str

    ## USER DATACLASS

      @dataclass
      class User:
        username: str
        password: str
        movieCollection: list


    =================================================================

    # IF YOU'RE ON M7 you should implement persistence. You should be storing all of your information to a .txt file.
    You are expected to be able to read from, write to, update, and delete from this file.



# EXAMPLE OUTPUT BEFORE M6:

```
What is your name? Logan

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? L

What is your name? Logan

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? A

Movie name: Movie A
Directed by: Director A
Movie A was added to Logan's collection!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? A

Movie name: Movie B
Directed by: Director B
Movie B was added to Logan's collection!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? V

Logan's Movies:
 - Movie A directed by Director A
 - Movie B directed by Director B

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? U

Current Movie Name: Movie A
Movie Name: Movie C
Director: Director A
Successfully updated!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? D

Movie Name: Movie B
Successfully removed movie!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? V

Logan's Movies:
 - Movie C directed by Director A
```

==================================================

# EXAMPLE OUTPUT FOR M6 ONWARD:

```
What is your name? Logan
Password: D!4boLiCAl

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? L

What is your name? Logan
Password: D!4boLiCAl

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? A

Movie name: Movie A
Directed by: Director A
Movie A was added to Logan's collection!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? A

Movie name: Movie B
Directed by: Director B
Movie B was added to Logan's collection!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? V

Logan's Movies:
 - Movie A directed by Director A
 - Movie B directed by Director B

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? U

Current Movie Name: Movie A
Movie Name: Movie C
Director: Director A
Successfully updated!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? D

Movie Name: Movie B
Successfully removed movie!

Would you like to [A]dd, [V]iew, [U]pdate movie, or [D]elete
from your collection, or [L]og out? V

Logan's Movies:
 - Movie C directed by Director A
```
