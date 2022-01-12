Django Music Collection 🎵

Create an application to keep track of all the music albums you own. 

-[] You can choose whatever fields you think an album should have, but it should have at least these three:
    title
    artist
    created_at

The created_at field should reflect the time that the album object is created (not the year that the album was released, although you could certainly create a field for that too!).

Your Django app should allow you to do the following:

    See a list of all albums on the homepage
    Create a new album
    See a detail page for one existing album
    Edit an existing album
    Delete an existing album

Your app should have at least minimal styling. It's pretty practical to use a CSS library like Tachyons or Picnic, though you can write custom CSS if you want to. Just remember that for this assignment, functionality is a higher priority than styling.

A good place to start is planning out your Album model and making sure you can make an Album object in the shell and/or admin. Make a couple of them. Then, you can start working on urls and views by make a homepage to list the existing albums.
URLs

Your app should have the following URLs. You'll need to define view functions to go along with each path. Remember, one view function can handle more than one type of request!
path 	verb 	purpose
"" 	GET 	show a list of all the albums
/albums/new 	GET 	show a form to create a new album
/albums/new 	POST 	create a new album
/albums/<int:pk> 	GET 	show details about a single album
/albums/<int:pk>/edit 	GET 	show a form to edit a new album
/albums/<int:pk>/edit 	POST 	update a specific album
/albums/<int:pk>/delete 	GET 	show a confirmation screen to delete a specific album
/albums/<int:pk>/delete 	POST 	delete a specific album

❓ Why are we using POST instead of DELETE or PUT/PATCH verbs for the delete and update actions? It's because we are using web forms to send the data. Web forms can only send GET or POST requests. (We have more options with AJAX, but we haven't learned about how to use that with Django yet.)
