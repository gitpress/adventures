# HTML5 Structural Elements

The development and increased adoption of HTML5 standard has seen many HTML elements added, redefined or dropped. In this section we will quickly go through the major new structural elements that have been added. 

These elements replace using dividers with identifiers and indicate the common structure of a webpage.

In order to get a sense of the old vs the new here are two examples of pre and post HTML5 elements:

```html
<!-- pre-HTML5 page -->
<body>
  <div id="nav"> 
    | <a href="#"> Home </a> | 
  </div>
  
  <div id="article">
    <div id="article-header">
      <h1>How many divs man?</h1>
    </div>
    <p>hard to pinpoint those differences easily</p>
  </div>
  
  <div id="footer">Totally written by a not bad but easily mistaken egg</div>
</body>
```


```html
<!-- example of a HTML5 page -->
<body>
  <nav> 
    | <a href="#"> Home </a> | 
  </nav>
  
  <article>
    <header>
      <h1>Hello HTML5</h1>
    </header>
    <p>What a great experience</p>
  </article>
  
  <footer>Totally written by a good egg</footer>
</body>
```

As you can see, the idea behind the new elements is to provide HTML elements out of the box that cover common things many webpages have.

> The **<div></div>** tag is a way of creating an editable and styleable area. To find out more about this see [section 12 - CSS](#)

## Nav

## Article

## Section

## Footer