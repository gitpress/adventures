## 1. Installing Middleman

 

To get Middleman working we need to download the gem. First create a file which we can work in for the rest of the book:

 

```shell
# CLI command to create a file and move into the directory
mkdir middleman && cd middleman
```

> If you are using Windows this command won't work because of the operator &&. If you must use Windows I recommend installing a Linux-y command line tool to follow along. You can also install git bash and use that.

> Alternatively, you can work through your browser and connect to a Linux box using one of the many in-browser IDEs. I personally do this all the time and find it a great experience for when I am on a Windows machine. My personal preference is to use [Codio](http://www.codio.com), as it has a brilliant free tier and is the most reliable.

Now download the Middleman gem:

```shell
# download the middleman gem
gem install middleman
```

this downloads the necessary files. It may take a while due to documentation so feel free to brew yourself a cup of tea. 

If you are using a ruby version manager like rbenv you may need to refresh your gemset. Using rbenv this command is:

```shell
# refresh your rbenv gemset
rbenv rehash
```

Right, you should now have a ready to use Middleman gem. We now have at your fingertips the ability to run Middleman commands.

 

## 2. Initilizing your first Middleman site

 

Let's build that site already!

 

Run the middleman init command to create a project with the name of your choosing:

 

```shell

# use middleman init command to create your site

middleman init mimp

```

 

As you may have noticed, the name after the **middleman init** command is where you write your project name. If it has more than one word use the Ruby tradition of "snake_case" rather than "camelCase".

 

This command will create a folder named after your project name as well as create a gemfile from which it will download some additional gems.

 

> INSERT IMG and EXPLANATION IF NEEDED of files

 

Let's move into the newly created folder to get building. For me I run:

 

```shell

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

 

```ruby

source 'https://rubygems.org'

 

gem "middleman", "~>3.3.7"

 

# Live-reloading plugin

gem "middleman-livereload", "~> 3.1.0"

 

# For faster file watcher updates on Windows:

gem "wdm", "~> 0.1.0", :platforms => [:mswin, :mingw]

 

# Windows does not come with time zone data

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

```html

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

 

## 3. Running your first Build

 

Ensuring you are in your project folder (mine being /mimp), run the following command:

 

```shell

bundle exec middleman build

```

 

This will create the static site from your ruby, embedded ruby HTML, JS and CSS and YAML. The output is created in a build folder which is easy to export to a webserver like Apache or Nginx.

 

Move into the build directory and double click the index.html file. The site now looks something like this:

 

> {{{{INSERT IMG HERE}}}}

 

Not exactly the most attractive site in the world but a working example. In the next chapter we will add bootstrap styles