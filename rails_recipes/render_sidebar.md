In order to render  seperate sidebar per certain actions you need to create two yields. One for the body, and the other for the sidebar.

```rails
<html>
  <head>
  </head>
  <body>
  <div class="container">
  <div class="col-md-8">
    <%= yield %>
  </div>
  
  <div class="col-md-4">
    <%= yield :sidebar %>
  </div>
  
  </div>
  
  </body>
</html>
```