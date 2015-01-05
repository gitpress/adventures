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

Now, we haven't done a lot but we have just included a lot of powerful SCSS into our project.

Before we crack open the champagne, we need to include the Bootstrap js and jquery.

## Delete the default styles

## create a master .scss file

## Get bootstrap styles

> you can also require bootstrap files through a gem!

## Include them in the local file

## Update basic webpage to have the structure of Bootstrap and test

## Build header and footer partials
