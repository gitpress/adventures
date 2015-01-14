# Running your first Build

Ensuring you are in your project folder (mine being /mimp), run the following command:

```bash
# run the middleman build command conforming to the Gemfile
$ bundle exec middleman build
```

> **bundle exec** is a command using the application dependency [bundler tool](http://bundler.io/). Basically, Bundler makes sure your gems don't conflict with each other. So when you run it, it checks your gemfile and ensures nothing breaks your program.

This will create the static site from your ruby, embedded ruby HTML, JS and CSS and YAML. The output is created in a build folder which is easy to export to a webserver like Apache or Nginx or your own hosting solution using SFTP.

> A great option is also jusing Github Pages! (Github){https://www.github.com} offers free static website hosting  which is a great deal. Later on in this book we'll cover exporting a project to github.

Move into the build directory and double click the index.html file. The site now looks something like this:

> {{{{INSERT IMG HERE}}}}

Not exactly the most attractive site in the world but a working example. In the next section let's make it more interesting.