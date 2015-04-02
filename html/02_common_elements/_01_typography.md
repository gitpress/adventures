# HTML Typography

I am taking Typography here to mean the very broad sense of writing or arranging things to "print" out the written word.

Much like a a printing machine, we wrap words and letters within these HTML tags to "print" out text to our screen in a meaningful and structured way.

> When you encounter the word Typography in connection with the web, it is often in relation to changing fonts, or the finer elements of designing your website's space between letters etc. This isn't what we'll cover in this chapter. This is about setting up our page to print out paragraphs, quotes and things like that

## inline and block elements

Generally speaking, an HTML element is either an inline element or a block element.

A block element is [https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements]()

An inline element is [https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elemente](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elemente)

## Headings

One of the most common elements you'll use is a heading or header. These are indicated by a "h" followed by a number (with a max of 6). 

To indicate something is the top heading in a page we wrap our text with ```<h1></h1>```. And to indicate a header of the lowest importance we use ```<h6></h6>```.

> HTML is what we call a **"case insensitive"** markup language. In plain English this means that it doesn't matter if you capitalize your tags or not. The browser just doesn't care. This is in contrast with nearly everything else you'll use to build products for the web. CSS, JavaScript, Ruby etc. all take capitalization very seriously.
>
> In HTML, H1 and h1 are the same thing. 
>
> In JavaScript, CamelCase and camelcase are not and you would experience errors if you expected them to refer to the same large African creature.

You should generally treat headings as gears in your car. You start with the first, move to second and then third. Whenever you start moving, you start low and progress up. So, if you need to start a new section you start and move up.

There is a slight caveat here. It is best to only use one ```<h1></h1>``` per page.

This is because things like "screenreaders" use them to understand the most important or defining header of a page. Basically, the title or essence of a page.

So, taking screenreaders into account it is best to reserve your ```<h1>First Heading</h1>``` to the most important title on your page.

This very book shows this in action. 

The name of the chapter or section starts with a ```<h1></h1>``` element, in this case **HTML Typography**, with each preceeding section using a ```<h2></h2>``` element to indicate the important sub-sections.

The available headings are therefore:

```html
<h1>Heading one</h1>
<h2>Heading two</h2>
<h3>Heading three</h3>
<h4>Heading four</h4>
<h5>Heading five</h5>
<h6>Heading six</h6>
```

> Include screenshot of elements in action

## Paragraph

Another integral HTML element is the paragraph. 

You won't write many websites without a paragraph here or there.

To make one you wrap each paragraph section between ```<p></p>``` tags - with p standing for paragraph naturally.

```html
<p>This is your first paragraph</p>
<p>This is the second</p>
```

> Include screenshot here

## Bold & Strong

One way of emphasising a particular word or phrase inline is to make it **bold**.

To do this we could wrap the word or phrase we want emphasising by making it bold with a set of ```<b></b>``` tags.

However, using the ```<b></b>``` tag is generally not seen as a good idea. 

The reasons are that If you are making something bold because it is a title, say withing a table, well a heading tag is more appropriate.

The other reason is that in HTML5 it doesn't convey any "semantic" meaning. Unlike the "emphasis" tag that we'll see later, it doesn't convey our desire to emphasize something and just looking at a word within a <b></b> tag we wouldn't instantly know why it is being emphasised.

The tag also just describes what we want a word to look like, and in modern HTML that job has been left to CSS, rather than a tag name. If we have ```<b></b>``` for bold why not ```<really-really-quite-massive-title-that-is-blue>How the English emphasise</really-really-quite-massive-title-that-is-blue>```

Let's say you do however want to emphasise a word within a paragraph that should be said strongly.

We can achieve this with the ```<strong></strong>``` tag. This tag wraps any word or text and communicates that the contained text should be said strongly like so:

```html
<p>There isn't any such thing <strong>Mr. Tibbles</strong>. If someone had invented a rug you could also wear, I would have heard about it!</p>
```

> image here

Here, unlike bold, we are communicating how the word should be communicated. This way has the added benefit of making sense to screen readers. That is, to the technology that communicates to people who cannot see. The use of the ```<strong>``` tag communicates the semantic meaning behind the word being emphasised.

## Italics & Emphasis

Another way we can emphasise text is through italics.

We do this by wrapping a word with ```<i></i>```.

## Underline

## Sup & Sub

## Linebreaks

## Headroom

## Blockquotes

## Abbreviations, Citations and Definitions

## Address