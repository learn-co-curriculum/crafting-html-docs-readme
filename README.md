# Crafting HTML Documents

## Problem Statement

So far we've been introduced to a lot of vocabulary and have had an
"experience" writing HTML.

In this lesson we're going to introduce you to some more essential HTML tags.

## Objectives

1. Identify patterns around tags, markup, and content
2. Define the document type tag: `<doctype>`
3. Define the HTML Content Area with the `<html>`, `<head>`, and `<body>` tag
4. Recognize an HTML Comment
5. Introduce the Most-Common HTML Elements

## Identify Patterns Around Tags, Markup, And Content

Every web page you've ever seen in a browser is the rendered output of HTML
that was requested by a browser.

HTML, or HyperText Markup Language, is a markup language which describes the
structure and meaning of web content. Web browsers, such as Mozilla Firefox,
Internet Explorer, and Google Chrome interpret the HTML code and use it to
create rendered output. Unlike Ruby, JavaScript and other programming
languages, markup languages like HTML can't process logic. You can't write in HTML:
"print this line 3 times" or "if it's Thursday, make the heading 'Baloney
Sandwiches for Lunch!'"

#### Tags

HTML consists of different markup _elements_ which are comprised of _markup_
that "wraps" _content_.  For example, say we wanted `Hello World` to appear as
a paragraph. We could use the `p` tag, which consists of an opening `p` tag
and a closing `p` tag. The content wrapped is `Hello World`. Here's the HTML
code:

```html
<p>Hello World</p>
```

Tags, like our `p` tags above, won't be displayed in the browser. Instead, they
affect how the content itself is displayed.

#### Attributes

We can also add `attributes` inside of the opening tag. For example, the `a`
element, which is used for links, has an `href` attribute to specify the
destination address of the link. If we wanted to link to
`www.flatironschool.com`, we could do so as follows:

```html
<a href="http://www.flatironschool.com">Flatiron School</a>
```

This would render as:

[Flatiron School](http://www.flatironschool.com)

Attributes will become especially important as we start working with the
Cascading Style Sheets (CSS) to make our pages look better.

#### Nesting of Elements

We also frequently nest elements inside of each other. To have a link displayed
as a separate paragraph, we could nest an `a` element inside of a `p`.

```html
<p>This <a href="http://www.google.com">link</a> will be a part of a separate paragraph.</p>
```

This would render as:

This [link](http://www.google.com) will be a part of a separate paragraph.

## Define The Document Type Tag: `<doctype>`

In the following steps we're going to create an HTML file. You might want to
use your Sandbox and type along.

We'd like to introduce you to a new tag, a tag that defines the _entire_ HTML
document. Its called the `doctype` tag. The HTML standard says that all HTML
documents begin with a "doctype declaration" tag. It should go very first.

If one is missing, most browsers pretend one is there, but you should always be
explicit and define it yourself.

The `doctype` tag tells our web browser which version of HTML to use. HTML is a
language that is still evolving. We might call that the doctype of _Romeo &amp;
Juliet_ is "Elizabethan English." The doctype of a speech by Barack Obama is
"Modern English." The two are more similar than different, but some things
aren't supported anymore.

Here's another surprise: not _all_ HTML tags have to be explicitly closed. Some
are considered "self-closing." Since it's not wrapping any content, our doctype
declaration doesn't require a closing tag.

To use HTML5, the current up-to-date version, we can simply write
`<!DOCTYPE html>` at the top of our HTML files.

```html
<!DOCTYPE html>

```

## Define The HTML Content Area With The `<html>`, `<head>`, And `<body>` Tag

Next, we add an opening and closing `html` tag. This tells the web browser to
interpret everything inside the tags as HTML code.

```html
<!DOCTYPE html>
<html>


</html>
```

HTML pages have two primary sections. They are the `head` and the `body`. The
`head` element contains metadata (or "data about the data") about the HTML
document and other information for the browser, while the `body` element
contains the actual content.

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- metadata about the HTML document as a whole -->

    </head>

    <body>
        <!-- content of our page will be here! -->

    </body>
</html>
```

## Recognize an HTML Comment

Let's also take a brief moment to recognize how to add comments into an HTML
document.  These won't get rendered to the browser at all: they're just helpful
notes for the author. We included two in the pevious section, they begin with
`<!--` and end with `-->`.

```html
<!-- NYC Pizza is world-famous, cheap, and loved by both vermin and human like! -->
<p>Top 5 Pizza Places in NYC</p>
```

This will render as:

Top 5 Pizza Places in NYC

Once this basic skeleton is in place, we're ready to start introducing content
that we can mark-up with HTML.

### Introduce the Most-Common HTML Elements

We've already looked at some common HTML elements, such as `a` and `p`. Let's
take a look at some more HTML elements.

#### Headers

HTML gives us access to different header elements, ranging from `h1` to `h6`,
with `h1` being the largest and `h6` being the smallest.

```html
<h1>Dogs!</h1>
<h3>Why Dogs are Great</h3>

<h6>Different Breeds</h6>
```

These would render as:

![Rendering of Dogs-centric HTML](https://curriculum-content.s3.amazonaws.com/web-development/crafting-html-docs-readme/rendered_example.png)

In addition to changing how the text is displayed, search engines use headers
to help determine what a web page is about.

#### Images

We can embed images on our web pages using the `img` element. The `img` element
doesn't have a closing tag. The `src` attribute tells the browser where to find
the image. The `alt` attribute will be displayed if an image can't be loaded,
and also describes the image to search engines.

The `alt` tag presents a moment to talk about an important principle behind Tim
Berners-Lee's vision for the Web: it is _inclusive_. If you're using assistive
technologies because you have a sight impairment, you shouldn't be cut off from
the web.  If you're in a remote community where internet access is expensive,
you might choose to disable images, but not lose the web.

While an `img` will "work," honoring the Web's vision for openness and
inclusion requires that we provide the `alt` tag as well.

`<img src="URL_TO_IMAGE" alt="Picture of a Dog">`

The `<img>` tag is also an example of a self-closing tag. You don't have to
write:

`<img src="URL_TO_IMAGE" alt="Picture of a Dog"></img>`

#### Lists

We can make bulleted, or unordered lists, using opening and closing `ul` tags.
Inside, we can nest an `li`, or "list item" element for each item on our list.

```html
<h5>My Favorite Things in No Particular Order</h5>
<ul>
    <li>Coffee</li>
    <li>Vinyl Records</li>
    <li>Pickling</li>
</ul>
```

This would render as:

____

<h5>My Favorite Things in No Particular Order</h5>
<ul>
    <li>Coffee</li>
    <li>Vinyl Records</li>
    <li>Pickling</li>
</ul>
____

We can also make a numbered, or ordered list, using an `ol` tag.

```html
<h5>Top 5 Pizza Places in NYC</h5>
<ol>
    <li>DiFara Pizza</li>
    <li>Lucali's</li>
    <li>Sal and Carmine's</li>
    <li>Juliana's</li>
    <li>Joe's</li>
</ol>
```
Would render as:

____

<h5>Top 5 Pizza Places in NYC</h5>
<ol>
    <li>DiFara Pizza</li>
    <li>Lucali's</li>
    <li>Sal and Carmine's</li>
    <li>Juliana's</li>
    <li>Joe's</li>
</ol>
____

## Conclusion

With this you now have the knowledge to craft your own, simple HTML documents.
You should be feeling comfortable with the concepts of markup, tags, and
content. You've had some practice seeing HTML change rendered text.

With this lesson we've rolled in some of the "formal rules" of HTML.
While browsers _generally_ do a great job guessing what you
meant, we want to follow the guidelines to make sure we don't get any surprises.

Keep practicing!
