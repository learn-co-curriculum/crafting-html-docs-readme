# What is HTML? 

## Outline

1. HTML, or "HyperText Markup Language", is a markup language that web browsers use to determine the structure of content
2. We write HTML using tags to surround content.
3. Web browsers use HTML to determine how our content should be displayed.
4. Many search engines use HTML tags to determine what web pages are about. 
5. Explain the purpose of `html`, `head`, and `body` tags.
6. List some commonly used tags and explain their purpose (`h1`, `p`, `ul`, `ol`, `img`, `a`)

## Objectives
1. Explain what HTML is and why it's important in the context of web development
2. Read a basic HTML document and understand the structure
3. Understand and use basic HTML tags

## Lesson

To get started, fork and clone 

### What is HTML?

HTML, or Hyper Text Markup Language, is a markup language which describes the structure of web pages. Web browsers, such as Mozilla Firefox, Internet Explorer, and Google Chrome, interpret the HTML code and use it to render some output. HTML doesn't have any logic behind it, like Ruby and other programming languages. Instead, it simply surrounds content and tells web browsers how that content should be displayed.

More simply, HTMl is the language of the web. Every web page you've ever visited is structured using HTML code. Being able to read and understand an HTML document is one of the most important tools in a developer's toolbox.

### HTML Syntax

HTML consists of different elements, which consist of opening and closing tags. For example, say we had the content `Hello World` that we wanted to display as a separate paragraph. We could use the `p` element, which consists of an opening `p` tag and a closing `p` tag. 

```html
<p>Hello World</p>
```

We can also add any number of attributes inside of the opening tags. For example, the `a` element which is used for links,  has an `href` attribute to determine the address of the link. If we wanted to link to www.flatironschool.com, we could do so as follows:

```html
<a href="http://www.flatironschool.com">Flatiron School</a>
```

This would render as:

[Flatiron School](http://www.flatironschool.com)

We can also nest elements inside of each other. To have a link displayed as a separate paragraph, we could nest an `a` element inside of a `p`. 

```html
<p>This <a href="http://www.google.com">link</a> will be a part of a separate paragraph.</p>
```

### Basic Document Structure

Let's look at the basic structure of html code. HTML begins with a "doctype declaration" tag, which tells our web browser which version of HTML to use. To use HTML5, the current up-to-date version, we can simply declare `<!DOCTYPE html>`. 

```html
<!DOCTYPE html>

```

Next, we add an opening and closing `html` tag. This tells the web browser to interpret everything inside as HTML code. 

```html
<!DOCTYPE html>
<html>
	

</html>
```

Every HTML page is made up of two sections, a `head` and a `body`. The `head` element contains meta data and other information for the browser, while the `body` element contains the actual content which will be displayed. 

```html
<!DOCTYPE html>
<html>
	<head>
		<!-- data for the web browser will be in here -->
	
	</head>
	
	<body>
		<! -- content of our page will be here! -->
	
	</body>
</html>
```

### Common HTML elements

We've already looked at some common HTML elements, such as `a` and `p`. Let's take a look at some more basic HTML elements.

#### Header

HTML gives us access to different header elements, ranging from `h1` to `h6`, with `h1` being the largest and `h6` being the smallest. Header tags display text larger or smaller on our page and also tell search engines what our pages are about. 

```html
<h1>Dogs!</h1>
<h3>Why Dogs are Great</h3>
	
<h3>Different Breeds</h3>	
```

#### Images

We can embed images in our web pages using the `img` element. The `img` element doesn't have a closing tag. The `src` attribute tells the browser where to find the image. The `alt` attribute will be displayed if an image can't be loaded, and also describes the image to search engines.  

`<img src="URL_TO_IMAGE" alt="Picture of a Dog">`

#### Lists

Some other useful HTML elements are lists. We can make bulleted, or unordered lists, using opening and closing `ul` tags. Inside, we can nest an `li`, or "list item", element for each item in our list. 

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

We can also make a numbered, or ordered list, using an `ol` tag. This functions in the same was as our unordered list, only with numbers instead of bullet points.

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

#### Comments
We can also include comments in our HTML code. These won't get rendered to the browser at all: they're just helpful notes for the programmer. 

```html
<h5>Top 5 Pizza Places in NYC</h5>
<!-- This won't get rendered, just a helpful note -->
```



## Resources

[HTML Fundamentals](https://www.youtube.com/watch?v=tuDKQxfiXmY)
