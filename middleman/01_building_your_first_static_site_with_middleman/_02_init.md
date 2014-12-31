# Initilizing your first Middleman site

Let's build that site already!

Run the middleman init command to create a project with the name of your choosing:

```bash
#use middleman init to create the site
middleman init mimp
```

As you may have noticed, the name after the **middleman init** command is where you write your project name. If it has more than one word use the Ruby tradition of "snake_case" rather than "camelCase".

This command will create a folder named after your project name as well as create a gemfile from which it will download some additional gems.

> INSERT IMG and EXPLANATION IF NEEDED of files
 
Let's move into the newly created folder to get building. For me I run:

```bash
# Because my project was called mimp, I change directory into that folder
cd mimp
```

You should now see four files and a source folder. Your directory looks something like this:

* /source
* .gitignore
* config.rb
* Gemfile
* Gemfile.lock

Let's work from the bottom up. 

#### Gemfile.lock

Your Gemfile.lock is there to lock down the versions of Gems that you used to create the project and your various dependencies.

#### Gemfile

If you have a decent background in Ruby or Rails you will know what a Gemfile is. It is essentially your place to indicate what Gems you want to use for your project and if needed, the specific version or source for each gem.

On your initial load your gemfile will look something like:

```Ruby
#Example Gemfile with comments removed
gem "middleman", "~>3.3.7"
gem "middleman-livereload", "~> 3.1.0"
gem "wdm", "~> 0.1.0", :platforms => [:mswin, :mingw]
gem "tzinfo-data", platforms: [:mswin, :mingw]
```

At the moment we have the default gems but we'll soon edit it to add some more interesting functionality like blogging ability.

#### config.rb

This file is where you get to set up how you want your Middleman tool to work for you. As we go through this book we will make changes to this file but feel free to choose what works for you.

This includes enabling relative URLs, choosing whether certain pages have different layouts (templates) and utilzing other helper methods and tools.

> A list of the options and things you can tweak are available on the [Middleman website](http://middlemanapp.com/) in various sections.

> In chapter x, I go through some possible options as well {{{INSERT LATER}}}

#### /source

This directory is where you will write your HTML, CSS and JS.

Inside you will see futher folders for images, javascripts, layouts and stylesheets which are all pretty self explanatory

 

> Explanation anyway. Example of layout included:

```erb
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <!-- Always force latest IE rendering engine or request Chrome Frame -->
    <meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible">
    <!-- Use title if it's in the page YAML frontmatter -->
    <title><%= current_page.data.title || "The Middleman" %></title>
    <%= stylesheet_link_tag "normalize", "all" %>
    <%= javascript_include_tag  "all" %>
  </head>
  
  <body class="<%= page_classes %>">
    <%= yield %>
  </body>
</html>
```

you will also see an ebedded ruby HTML page that, on using the Middleman build command, will get wrapped into its layout.

 

You will also see some YAML at the top of the page which provides useful information to a template, like the title page etc.

 

```yaml

---

title: Welcome to Middleman

---

```

 

Lets see that work.
