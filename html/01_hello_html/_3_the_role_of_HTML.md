# The role of HTML

HTML provides the foundations or structure to websites. It is a "markup" language that defines what a browser needs to display.

It looks like this:

```html
<p>Hello World!</p>
```

HTML is used to communicate to browsers, and related products, how things should be constructed.

```html
<p>Some things <strong>need</strong> extra focus</p>
```

Take a look at a Newspaper or a book. Inside that you'll see headings, sub-headings, paragraphs. You may also see areas assigned for images. If you have an academic treatise nearby, you may also see a footer where references are made to ramblings of other academics.

In a printed book, the headings, the footer, the paragraphs all communicate a structure that helps create a common pattern so that readers (you and I) are able digest and navigate through a book's information.

HTML provides the structure similar to that we find in a book, but on a webpage or app. HTML wraps content (literally!) and the browser communicates the structure to us. 

So, when you write HTML you are building the structure into which information, data, is injected. Your structure is vitally important to the readability and usefulness of your document to a reader. Your HTML is vitally important to ensure your document creates a structure that is consumed in the way you intend it to be consumed.

```html
<article>
  <header>A letter in aid of the advancement of Cat Herding 
     - Archibald Whiskers III</header>
  <p>It is in my estimation that laptops are an emergent 
     threat to Cat Herding everywhere. It is not possible, nor 
     likely, that Cat Herding can commmence as it is did the 
     days of my Great Uncle* when just any common person may be 
     able to attract Cats to screens and laptop keyboards 
     without effort. It is therefore my opinion that...</p>
  <footer>*important note</footer>
</article>
```

HTML is the common structure of the web. It is a way of telling browsers how to build something, what to put in certain containers and what containers belong in certain silos.

HTML doesn't do it alone. We have CSS (Cascading Style Sheets) which provides the styling and JavaScript which adds a layer of interactivity and polish to use too. This book won't really directly focus on those two technologies (forthcoming books will though!) but it will give you the ability to start leveraging them soon enough.

## Tag you're it!

HTML marks up your content with tags. The most common form of tag is the opening and closing tag where you indicate the start of a section and then the close with two tags like this:

```html
<p>This is a set of p for paragraph tags</p>
```
The first paragraph tag starts the markup. The last paragraph tag with the forward slash indicates where it ends. And that is pretty much the essence of HTML. You'll learn the tags pretty quickly and we'll cover them in the second chapter completely.

> Tag team cartoon here

There are some tags that don't tag team. These tags are the lone wolves of HTML tags and they "self close". The most common of these is the one for images. This dangerous lone wolf looks like:

```html
<img src="yourhilariousbabyphoto.jpg">
```

So, the **<img>** tag completes itself, it doesn't require a closing **</img>** tag to come with it. If this seems daunting, don't worry. You'll soon get a grip on the select few tags that work this way. You will make mistakes but every developer does, just keep trucking away.

Now you may have noticed something  with that last example. The source or src *attribute* inside the **<img>** tag. This is something that really makes HTML super-powered.

## Awesome Attributes

Those additional things inside a HTML tag are called attributes. Attributes allow your HTML tags to call in additional resources to identify themsevles to be transformed by JavaScript. They are very important.

Like the rest of HTML, they are simple additions which take a little time, and trial and error, to get a grips on.

One of the most common attributes is that which you need to add to an **<img>** tag called **src=**. Src stands for source and is where, inside double quote, you indicate where the image is located.

```html
<img src="imgs/cute-cat-photo.png">
```

Another common attribute is **href=**. Href indicates where a link should go. A link is actually designated by an anchor tag, as below:

```html
<a href="http://www.alleyooop.com"> This is the text that appears! Press me!</a>
```

Here the href indicates the website that clicking a link will go to. The text between the **<a></a>** is the "hyperlinked" text; the blue underlined text that when you click it goes to another page you have likely seen plenty of times before:

> {{{{ INSERT IMG HERE }}}}

Attributes also provide additional information about a link or image. A clear example is adding alternative text to an image so that when people hover over it they get a text based explanation. You include it like this:

```html
<img src="imgs/cute-cat-photo.png" alt="a cute cat pic">
```

The **alt=** attribute provides you with the ability to add some extra info. This alternative text is also helpful for people with visual problems. 

By providing some alternative text you can at the very least provide some additional context to your image for screen readers.

## A quick recap

Right, so HTML provides structure or markup to a document. This markup indicates to a browser (or other product) that something is a header or a paragraph or even an image or link by the tag it uses.

If you want something to be a paragraph you wrap it with **<p></p>** tags. Most tags work like this.

Some tags don't wrap text. An example of this is the **<img>** tag which is self-contained.

Tags like **<img>** also feature attributes inside them.

These attributes call other resources
