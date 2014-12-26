# Writing some HTML

About time? Ok, crack open your text editor of choice 

> Not MS Word okay! If you skipped the section about text editors and didn't install or get a developer friendly text editor time to take a detour and do that.

In a new file write the following:

```html
<!-- path: hello.html -->
<!DOCTYPE html>
<html>
  <head>
    <title>Cat Herding 101</title>
  </head>

  <body>
    <h1>Hello world!</h1>
  </body>
</html>
```

Save the file as **"hello.html"**. Make sure you save the file as a .html file. If you saved the file and it is called something like hello.html.txt remove the .txt to make it a real html file.

On your computer you'll likely see your .html file adopt the icon of your browser of choice

{{{{{{ INSERT IMG }}}}}}

Double click it and admire your awesome awesomeness!

Did everything appear as you expected?

The content between the **<title></title>** tags didn't show up on the page. The reason for this is that the title tags designate the *title* of your html document to the browser (and not the title of a paragraph etc.). If you look at your browser tab you should see it:

{{{{{{{{ INSERT IMG }}}}}}}}

Everything that goes between the **<head></head>** tags typically doesn't render onto the page. This is where you place important data, set certain configuration details (like the language the document is written in) and include any stylesheets and JavaScript files.

A typical **<head></head>** section can look something like this:

```html
<!-- Example of a more complete head section -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My HTML Page</title>
    <link rel="stylesheet" href="css/style.css">
  </head>
</html>

```
So, lets go through the rest of the things we have introduced in this chapter:

### <!DOCTYPE html>

defines the document that you are writing is seen as a modern, HTML5 document. This is opposed to a HTML4 or XHTML document which were previous standards of HTML.

> To read more about HTML5, how it emerged and past standards see here: [linkage]()

### <html></html>

The HTML tag indicates where the HTML document starts and ends. 

The tag is often used in conjunction with what is called an "attribute" which defines the language. In our previous example we defined it as **<html lang="en"></html>** which is **lang=** (the attribute) and then within quotes the language you wish to define (the value).

{{{{{ IMG HERE EXPLAINING ATTRIBUTE KEY AND VALUE }}}}}

### <head></head>

We've seen the head tag before, as mentioned it provides general information - often called metadata - about the html document, such as its title and links to scripts and stylesheets.

### <meta>

This tag, which is one of the cases where you don't have a closing companion tag, indicates values such as which character set to use, which version of Internet Explorer to use if possible, the author of the document and the a brief description of the following content.

The meta tag is used to represent any information that isn't already explained by the other tags in the head section.

> For more information about what attributes can be used within the **<meta>** tag, see the [Mozilla Developer Network documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta)

### <title></title>

The title tag is another that we have already covered. The tag provides the title for the entire document and is used to name the tabs on modern browsers like so:

{{{{{{{ IMG HERE }}}}}}}

> If you are wondering how those lovely little icons are provided you use a **link** tag, which we will cover shortly, ensuring you define the image with the attribute of rel= with the value of "icon" like so:
> ```html
<!-- example of a icon link -->
<link rel="icon" type="image/png" href="http://example.com/myicon.png">
```

### <link>

The link tag lets you draw in any additional resources like stylesheets to make things pretty or JavaScript files to add interaction and data manipulation.

With the link tag, and as with many html elements, the real value comes in the attributes. The rel= indicates what type of file is being linked to - in the case below a stylesheet. The href= attribute tells your document where it can find the resource you are linking to.

```html
<!-- Example of a stylesheet being included through the link tag. -->
<link href="style.css" rel="stylesheet">
```

This file is located in the same directory or folder of its HTML file. For this example, looking something like:

> image

To link things outside of your folder you must indicate the location of your spreadsheet. 

If you decided to put your spreadsheet in a file called css then your link tag could look like this:

```html
<!-- Example of a stylesheet being included from a different folder -->
<link href="css/style.css" rel="stylesheet">
```

It is worth mentioning the two ways of telling your document where it can find the resource you are telling it to include: absolute and relative linking.

An absolute link is where you provide the entire link to a resource. A good way of thinking about this is that you provide the full URL, so instead of style.css you put http://www.address.com/styles/main.css If you moved your HTML file to another website address it could still technically find the CSS file.

```html
<!-- Example of an absolute link -->
<link href="http://alleyoop.com/public/css/style.css" rel="stylesheet">
```

A relative link is where you provide where the file is, relative to the directory of the HTML file. So, from your base folder your **style.css** is inside a css folder so your link shows:

```html
<!-- relative link example -->
<link href="css/style.css" rel="stylesheet">
```

The benefit of a relative link is that it is often faster and more transferable. If you have been creating some links on one URL but move your project over to another then a relative link should remain the same. However, an absolute link with break.

> It can take a little trial and error to really get this concept down. An absolute link is like providing someone who wants to know where your Nan lives her entire address and post code. From wherever that person may be, she should be able to find her. 

> A Relative link is where you reply "She lives five doors down". This makes sense, and is extrememly fast and efficient, when someone is outside your door on your street that is. It doesn't however help if they are not in your local area.

### <body></body>

The body tags wrap the main content of your html document and is where most of the action takes place. Generally speaking you take little notice of this tag but it is vital for your browser to recognize and build a proper representation of your HTML to any visitor.

### <h1></h1>

Within your body section we have a heading tag. Headings range from heading 1 **<h1></h1>** to heading 6 **<h6></h6>**

As expected, your first heading should correspond to **<h1></h1>** and each section with a heading should have a heading that falls below that.

Here is an example of how to use headings:

```html
<!-- An example of using h1 to head up a document and h2 to show the sections within -->
<body>
  <h1>Welcome to my awesome webpage</h1>
  <p>I have a lot of great moving widgets for you to see.</p>
  
  <h2>Blinking Widget</h2>
  <p>...</p>

  <h2>Flashing Widget</h2>
  <p> ...</p>

  <h2>Annoying Sound Widget</h2>
  <p> ...</p>
</body>
```

Here my **<h1></h1>** tag shows the visitor my webpage's overriding reason to exist, while my **<h2></h2>** tags head up the sections about my finely crafted widgets.

> Getting headings right is important. Not only do Search Engines like Google use them to understand your document, people often skim them to find the information they want. Correctly choosing headings is therefore vital.

When it comes to headers make sure to use them in as natural a sequence as possible. If you have a sub-header within a **<h2></h2>** section you shouldn't use a **<h1></h1>** tag.

```html
<!-- An example of the best use of sub-headings within a html doc -->
<body>
  <h2>Blinking Widget</h2>
  <p>...</p>
  <h3>How to contact me about my widget</h3>
  <p> ...</p>
</body>
```

Here we are using the **<h3></h3>** tag as a sub-header which gives our HTML the right structure and presentation.

> Think of headers within a section being like gears in a car. You should move naturally up from gear 1 to 2, to 3. When you start a new section, start again from a low heading and again move up gradually.

## Body

## Charset & Meta

## Typography

## Paragraphs