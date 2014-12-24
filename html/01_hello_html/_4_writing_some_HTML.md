# Writing some HTML

About time? Ok, crack open your text editor of choice 

> Not MS Word okay! If you skipped the section about text editors and didn't install or get a developer friendly text editor time to take a detour and do that.

In a new file write the following:

```html
<!-- hello.html -->
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

#### <!DOCTYPE html>

defines the document that you are writing is seen as a modern, HTML5 document. This is opposed to a HTML4 or XHTML document which were previous standards of HTML.

> To read more about HTML5, how it emerged and past standards see here: [linkage]()

#### <html></html>

The HTML tag indicates where the HTML document starts and ends. 

The tag is often used in conjunction with what is called an "attribute" which defines the language. In our previous example we defined it as <html lang="en"></html> which is lang= (the attribute) and then within quotes the language you wish to define (the value).

{{{{{ IMG HERE EXPLAINING ATTRIBUTE KEY AND VALUE }}}}}

#### <head></head>

We've seen the head tag before, as mentioned it provides general information - often called metadata - about the html document, such as its title and links to scripts and stylesheets.

#### <meta>

This tag, which is one of the cases where you don't have a closing companion tag, indicates values such as which character set to use, which version of Internet Explorer to use if possible, the author of the document and the a brief description of the following content.

THe meta tag is used to represent any information that isn't already explained by the other tags in the head section.

> For more information about what attributes can be used within the **<meta>** tag, see the [Mozilla Developer Network documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta)

#### <title></title>

The title tag is another that we have already covered. The tag provides the title for the entire document and is used to name the tabs on modern browsers like so:

{{{{{{{ IMG HERE }}}}}}}

> If you are wondering how those lovely little icons are provided you use a **link** tag, which we will cover shortly, ensuring you define the image with the attribute of rel= with the value of "icon" like so:
> ```html
<link rel="icon" type="image/png" href="http://example.com/myicon.png">
```

#### <link>

The link tag lets you draw in any additional resources like stylesheets to make things pretty or JavaScript files to add interaction and data manipulation.

With the link tag, and as with many html elements, the real value comes in the attributes. The rel= indicates what type of file is being linked to - in the case below a stylesheet. The href= attribute tells your document where it can find the resource you are linking to.

```html
<link href="style.css" rel="stylesheet">
```

It is worth mentioning the two ways of telling your document where is can find the resource you are telling it to include: absolute and relative linking.

absolute - This is where you provide the entire link to a resource. A good way of thinking about this is that you provide the full URL, so instead of style.css you put http://www.address.com/styles/main.css If you moved your HTML file to another website address it could still technically find the CSS file

> Aboslute link is like providing someone who wants to know where your Nan lives here entire address and post code. From whereever that person may be, she should be able to find her. Relative link is where you reply "She lives five doors down". This makes sense, and is extrememly fast and efficient, when someone is outside your door on your street. It doesn't however help when/if they are not in your local area

## Head

## Body

## Charset & Meta

## Typography

## Paragraphs