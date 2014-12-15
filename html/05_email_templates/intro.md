# Creating HTML Email Templates

In this chapter we will go through building a common product that uses HTML; an email template. We send and recieve countless emails throughout the day, at home, on the move and at work. Though some emails are plain text and not HTML, the majority are HTML and when it comes to being paid to build for the web, you don't often get paid to build things in plain text.

There is however, a bit of an issue. Even more so than web browsers, the products that render our emails are a massive mess. Not only can you NOT include external spreadsheets or styles outside of the HTML elements, many older but very popular email clients break normal, modern HTML. There is also an added issue in that version by version, products like Outlook will render your emails differently. Same code, completely different layouts because one product was made in 2005, and the other 2007.

Generally speaking, you have to code your emails like the late 1990s and use tables to structure everything. The three main rules of HTML emails are:
1. No modern CSS or HTML. Tables everywhere
2. You must put things inline. No external styles or scripts
3. Every client is radically different. A button may render on one version, but not render on another at all

## Setting the scene

Before you build a product you must scope out what you need to design and what success looks like. To put it another way, not knowing why you are building something isn't a great way of spending your time.

We'll build something pretty simple: An email advertising this very book!

Our target audience will be people who have signed up to recieve an update on this book being released. This group of people need to be told how to get the book. We'll assume they are already interested in the subject (having signed up for the book and all) so we can keep the details light.

We'll want something that looks modern but reflects the personality of the book too.

We'll want to track how many people opened the email or clicked the links so we can track the success of the email and track that against how many new downloads.

Therefore our key features are:
* highly focused email that talks only about the book release
* Ensures the reader knows how to easily download/get the book
* Includes opening and tracking functionality so we get a picture of how successful the email was

## Wireframing the email

Having some notion of what the email is trying to do (inform people about the download) and what success looks like (lots of clicks and downloads) it is worthwhile sketching out what we want our email to look like.

First I have put pen to paper and scribbled out something that looks decent.

INCLUDE_IMG_HERE

It follows a pretty traditional pattern for emails and gives prominence to the main goals of the email (apart from the tracking but we'll get to that in a bit). 

> Along your journey to becoming a web developer and/or building products for the web you'll need to get some sense for design. I keep a google presentation of website elements and components that I like A great place to start by looking at pretty things is [Dribbble](http://www.dribbble.com). [Pinterest](htttp://www.pinterest.com) is another good resource for images of people's designs. As ever, give reference to anything that inspired you on your journey.

## Scaffolding the html

#### Step one - 

#### Step two -

## Ensuring we track everything

