# A bit of CSS

This book will not focus on giving you a thorough grounding in CSS but any discussion of HTML would not be complete without touching on the tool used to style websites.

CSS or Cascading Style Sheets, is, as I mentioned, used to style your HTML elements. It gives your HTML the colour, shape and position (hence the Stylesheet name).

The cascading part of CSS refers to the fact that each CSS file starts from the top and goes down. The reason this is important is that is informs how your elements may be styled if you have two rules for one thing. 

A better way of explaining this may be to look at some CSS.

The following code is some basic CSS that takes the p or paragraph element and changes its default browser colour:

```css
p {
  color: white;
}

p {
  color: red;
}

p {
  color: blue;
}
```

In this example we have set the paragraph element to a specific colour three times. What colour do you think it will be?

The answer is blue. A CSS file sets your styles from the top down and something you'll notice about computers is that often the last assignment is final. There are exceptions to this rule and ways of circumventing but, all things being equal, when it comes to CSS, the last assignment of an element wins.

> If you spell colour "colour" you may have noticed that in our CSS we spell it the American way. If that pains you, sadly this is just what you'll have to get used to. Similarly, things like centre need to be written center. If that doesn't bother you, don't worry about it. If it does, time for the stiff upper lip.

## How CSS is constructed

CSS is pretty simple at its heart. However, it can like most things in web development, be difficult to master. With CSS you'll soon find yourself able to hack around though and build pretty things.

The most basic rules of CSS have already been shown in the previous paragraph example. That is, you:
1. Define the element/thing you want to style
2. You write some curly braces like so {} after the element/thing
3. Inside those braces you define a feature, write a colon and then the corresponding value ending with a semi-colon to indicate that you have finished writing a value

{{{{{ IMG HERE REAFIRMMING THE SET UP}}}}}

## Defining some elements


## CSS IDs

CSS IDs are powerful namespaces or identifiers. They indicate to a browser a key section. Before HTML5 and the HTML elements of <article></article> etc. IDs would set things up like:

```
<div id="article">
<h1>And thank you for all the fish! - Dolphin</h1>
</div>
```
Since the new HTML5 elements have arrived it is less important to mark out sections with IDs (though this is still pretty common and you'll likely see it for years to come). 

However, they are still used as powerful identifiers in conjunction with JavaScript, server side code, specific CSS rules or custom sections.

Imagine you have a lot of articles on a page but every once in a while you feature an advert. Because the Journal of Cat Herders are paying you a lot, an extra for every click, you give them a custom style.

One way of indicating the custom area and leveraging CSS to markup the section differently would be to use an ID like so:

```html

<article>
<h1>How I learnt to stop worrying and love stuff</h1>
...
</article>

<article id="advert">
<h1>10 ways to take your Cat Herding to the next level</h1>
...
</article>
```
With the Cat Herders' advert identified by an ID you could then write some custom CSS.

```css
#advert h1 {
  color: red;
}

h1 {
  color: grey;
}
```

Before you ask, yes the hashtag indicates an ID (so in CSS a # means "something with the id of" ).

Can you guess what happens to the heading of the advert?

{{{{{{{ INSERT IMG }}}}}}}

As you can see, the advert's heading is red but not the other article's heading. 

So an ID says "Whatever is defined inside my domain, can be different without changing other people's elements".

So IDs have the ability to have alternative rules set within them. This is what is meant by a "namespace".

Your ID sets a namespace of "#advert" and everything within that can have its own set of rules. This is a bit like visiting your partner's parents for Christmas. Lots of the same things - Monopoly, Christmas Crackers, Carades - just different family-specific rules.

You may remember earlier that I said that CSS takes the last definition as final. So this is one way of getting around that.

As with any thing powerful however, use this with caution. It may be easier to use a class.

Although most browsers will forgive the existence of more tha one ID per page, it is bad practice to use the same ID twice. Using the same ID twice can also break any JavaScript and as you become a web developer, you don't want to have to deal with easily avoidable issues with your CSS

> So, when to use IDs? They are really powerful namespaces or family indictors so whenever you need a one off but extremly important section it is valuable to use one.

## Classes




## Responsive Design

The technique of responsive web design (or RWD) is a little beyond this book, though the concept is not. Essentially, RWD is the collection of techniques where a web page responds to the size of the users' screen or browser size.

Essentially then, a website is programmed to check is this screen over or under 800 pixels. If it is under, reduce the size of things and stack them on top of each other, if it is over stay the course.

