#Scaffold our website

In this section we are going to add bootstrap to our project and scaffold our basic site layout.

The first thing we need to do is remove the default styles that come with our project. Delete the normalize.css and all.css files from the ~/source/stylesheets/ folder.

Let's call our central SCSS file the rather uninspiring but conventional ```main.scss```

your stylesheet directory should contain these files:

* main.scss

> If you are an aspiring command-line warrior, on Linux systems you should be able to create a file with the ```touch``` command. So, within the folder you want to create a file run ```touch main.css```

The next thing we want to do is add our bootstrap CSS files. We could do this via a Gem but I like to hack around with my SCSS and JS in directory and I think it aids the learning curve to see professional code in your directories as much as possible.

Create two files called ```_variables.scss``` and ```_bootswatch.scss``` within your stylesheets folder.

your stylesheet directory should now contain these files:

* main.scss
* _variables.scss
* _bootswatch.scss

We don't currently have anything in those folders so let's get to the Bootswatch website and grab outselves a styled version of Bootstrap. I personally like a bit of material design so lets grab oureslves "paper".

On the [paper page](http://bootswatch.com/paper/) go to the download drop down and locate the two .scss file names. Press on each. They should download the .scss files locally. Either open them and copy the .scss into your newly created files or replace the files in your ```~/source/stylesheets/``` folder.

Let's update our ```main.scss``` file to include those two new files. To do this we need to include an ```@import``` command. 
```@import``` as you guessed, imports other files. We follow the import statement with the file we want to import inside some double quotes. Just like plain old CSS we end the line with a semi-colon. So, in our ```main.scss``` file, write the following:

```scss
@import "_variables.scss";
@import "_bootswatch.scss";
```

We also need to update our references to the layout file.

Navigate to ```~/source/layouts/layout.erb```. Edit the stylesheet_link_tag attribute to the following:

```erb
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    
    <!-- Always force latest IE rendering engine or request Chrome Frame -->
    <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible">
    
    <!-- Use title if it's in the page YAML frontmatter -->
    <title><%= current_page.data.title || "The Middleman" %></title>
    
    <%= stylesheet_link_tag "main" %>
    <%= javascript_include_tag  "all" %>
  </head>
  
  <body class="<%= page_classes %>">
    <%= yield %>
  </body>
</html>
```
This connects the ERB stylesheet tag helper to the file called main.scss and makes sure it is included on every html page.

Now, we haven't done a lot but we have just included a lot of powerful SCSS into our project.

Before we crack open the champagne, we need to include the Bootstrap js and jquery.

#### Include jQuery and Bootstrap.js

First navigate to [Bootstrap's website](http://getbootstrap.com/) and download the compiled assets.

> INSERT IMAGE bootstrap_download.png

In that download find the ```bootstrap.js``` file which is normally located in the ```~/bootstrap-x.x.x-dist/dist/js/``` folder. Copy it and include it into your Middleman project's javascripts folder.

Your ```javascripts``` folder should now look like:

* all.js
* bootstrap.js

The next thing to do is include jQuery. Go to the [jQuery website](http://jquery.com/download/) and download the latest 1.11.x version of jQuery. 

> jQuery support versions

Move that file into your ```javascripts``` directory as you did the bootstrap file.

> INSERT IMAGE download_jquery.png

Rename your ```jquery-1-11-2.js``` file to a cleaner named ```jquery.js``` .

Your ```javascripts``` folder should now look like:

* all.js
* bootstrap.js
* jquery.js

### Make sure the order is correct!

## Delete the default styles

## create a master .scss file

## Get bootstrap styles

> you can also require bootstrap files through a gem!

## Include them in the local file

## Update basic webpage to have the structure of Bootstrap and test

## Build header and footer partials
