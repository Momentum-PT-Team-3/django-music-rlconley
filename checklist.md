Django Music Collection 🎵

Create an application to keep track of all the music albums you own. 

1. You can choose whatever fields you think an album should have, but it should have at least these three:  
    title  
    artist  
    created_at  
        The created_at field should reflect the time that the album object is created (not the year that the album was released, although you could certainly                 create a field for that too!).  
    A good place to start is planning out your Album model and making sure you can make an Album object in the shell and/or admin. Make a couple of them. Then, you   can start working on urls and views by make a homepage to list the existing albums.  
- [ ]  Create an album model in models.py  
- [ ] Model needs these attributes
    - title -> CharField
    - artist -> CharField
    - created_at -> DateField  
    https://docs.djangoproject.com/en/4.0/ref/models/fields/#datefield  
- [ ] Make some sample albums in admin

2. Make the homepage. It should have a list of all the albums  
- [ ] make a `templates` directory, add it to settings.py TEMPLATES_DIRS
- [ ] make template (index.html), put some text on it
- [ ] add path to urls.py, that path should call the view for the homepage
- [ ] add view that accepts request and renders the index.html template & context


TODO:
Break down the rest below.


Your Django app should allow you to do the following:

    See a list of all albums on the homepage
    Create a new album
    See a detail page for one existing album
    Edit an existing album
    Delete an existing album

Your app should have at least minimal styling. It's pretty practical to use a CSS library like Tachyons or Picnic, though you can write custom CSS if you want to. Just remember that for this assignment, functionality is a higher priority than styling.


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
