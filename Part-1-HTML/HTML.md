Build Your Own Website - Part 1 - HTML
======================================

Synopsis
--------
In this part, we'll create our own webpage from first principles, learning in the process how web pages are built.

*Example files are numbered byow-XX.html where XX corresponds to the numbered headings below. Screenshots of how each set of HTML markup appears are included as byow-XX.png*

(1) Websites vs Apps
--------------------
Explain how websites are different from apps that you install on your phone or tablet - the instructions are stored on a server and only downloaded to the web browser when requested. By contrast, the instructions for an app are stored on the mobile device when you first download the app.

(2) Hyper Text Markup Language
------------------------------
Deconstruct 'HTML':
* Before the web, there were older mechanisms for retrieving data (gopher, etc.) but these did not have the means to link through to other pages or sites
* The web relies on HTML, or HyperText Markup Language
* 'HyperText' is special text which allows one page or site to link to another. The link is one-way
* 'Markup' just means that a special kind of code is applied to normal text, which is then interpreted by the web browser
* 'Language' because there are rules and syntax to be followed in order for the browser to understand what you mean by your HTML

(3) View Source
---------------
1. Go to http://www.wikipedia.org/ and select 'View Source' from the browser. This option can be found under:
	1. Google Chrome: right-click on page -> View page source
	1. Internet Explorer: right-click on page -> View source
	1. Firefox: right-click on page -> View Page Source
1. Look for the following lines:
	1. <html ...
	1. <head ...
	1. <title ...
	1. <body ...
1. We can see that a webpage is defined by lots of text instructions - this is HTML

(4) HEAD + BODY = Snowman!
--------------------------
1. Draw a large circle on a whiteboard, towards the bottom part of the page
1. Draw a smaller circle resting on the first one
1. What does this look like?
	1. A snowman!
1. Where do the snowman's eyes/nose/buttons go?
1. Similarly, HTML has:
	1. Head
	1. Body
1. The head and body sections each contain different HTML elements

(5) Example HTML
----------------
We're going to start with a basic 'snowman' webpage.

Open up a text editor:
* Notepad (Windows)
* TextEdit (OSX) - 

Enter the following text

```html
<!DOCTYPE html>
<html>
	<head>
	</head>
	<body>
	</body>
</html>
```
Ignore the reason for the first line containing `<!DOCTYPE html>` - this is a more advanced topic. For now, we just need to know that this first line means we're using the latest HTML version, HTML 5.

Save this file as `byow.html` on your computer, and then double-click on the file from within the file explorer to launch your web browser and view the file.

The browser will display a blank page, because at the moment, although our web page contains some text, it does not contain any *displayable* text, only markup.

(6) Title
---------
We'll now change the title of the page so that the browser displays the page title in the system menu.

Back in the text editor, change the text to look like this:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>BYOW - Build Your Own Website</title>
	</head>
	<body>
	</body>
</html>
```
Save the file, and refresh the page in your browser. You should see that the page title (in the tab, or in the system menu) now says 'BYOW - Build Your Own Website'.

(7) Heading
-----------
We'll now add a heading, making some text appear in the page.

Back in the text editor, change the text to look like this:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>BYOW - Build Your Own Website</title>
	</head>
	<body>
		<h1>I built my own web page!</h1>
	</body>
</html>
```
Save the file, and refresh the page in your browser. You should see that the page now displays a heading (in bold): 'I built my own web page!'.


(8) Font Style (Typeface)
-------------------------
Let's change the typeface to something more modern.

Back in the text editor, change the text to look like this:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>BYOW - Build Your Own Website</title>
		<style type="text/css">
			body {font-family: sans-serif;}
		</style>
	</head>
	<body>
		<h1>I built my own web page!</h1>
	</body>
</html>
```
That is, just after the `<title />` element, and within the `<head />` element, add the following markup:
```html
		<style type="text/css">
			body {font-family: sans-serif;}
		</style>
```

Save the file, and refresh the page in your browser. You should see that the typeface uses a sans-serif font. Instead of 'Arial' you can also choose 'serif', 'Monospace', or 'cursive'; there are more advanced options, but we'll not cover those here. 

(9) Images
----------
We'll now add an image to the page.

The important thing to know about images (and other multi-media files, such as Flash, and videos) is that they are not stored in the HTML itself, but are stored separately somewhere on a server, and retrieved and displayed by the web browser when it processes the HTML page.

Back in the text editor, change the text to look like this:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>BYOW - Build Your Own Website</title>
		<style type="text/css">
			body {font-family: sans-serif;}
		</style>
	</head>
	<body>
		<h1>I built my own web page!</h1>
		<p>Here is a picture of a cat:</p>
		<img src="http://upload.wikimedia.org/wikipedia/commons/4/4c/Lolcat.jpg" />
	</body>
</html>
```
That is, include the following markup just after the `<h1 />` element, and inside the `<body />` element:
```html
		<p>Here is a picture of a cat:</p>
		<img src="http://upload.wikimedia.org/wikipedia/commons/4/4c/Lolcat.jpg" />
```
The `<p>` element signifies a paragraph of text, and the `<img />` element directs the browser to include an image. The 'src' attribute tells the browser where to look for the image; in this case, we're taking the image from the Wikipedia website.

Save the file, and refresh the page in your browser. You should see the text 'Here is a picture of a cat:' followed by a large picture of a cat asleep.  

(10) Basic styles
-----------------
We'll now change the styles for the page to make the image display a bit nicer.

Back in the text editor, change the text to look like this:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>BYOW - Build Your Own Website</title>
		<style type="text/css">
			body {font-family: sans-serif;}
			img {border-width: 10px; border-style:ridge; width: 30%;}
		</style>
	</head>
	<body>
		<h1>I built my own web page!</h1>
		<p>Here is a picture of a cat:</p>
		<img src="http://upload.wikimedia.org/wikipedia/commons/4/4c/Lolcat.jpg" />
	</body>
</html>
```
That is, include the following markup just after the `body {font-family: sans-serif;}` declaration, inside the `<style />` element:
```html
		img {border-width: 10px; border-style:ridge; width: 30%;}
```
By including a style specification for 'img' items, we're asking the browser to display a border of 10 pixels (px), a ridged border style, and a maximum image width of 30% of the browser's window width.

Save the file, and refresh the page in your browser. You should see that the image is smaller and fits on the page.

(11) Hyperlinks
---------------
We'll now add a hyperlink to the page, linking to another (external) web page.

Back in the text editor, change the text to look like this:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>BYOW - Build Your Own Website</title>
		<style type="text/css">
			body {font-family: sans-serif;}
			img {border-width: 10px; border-style:ridge; width: 30%;}
		</style>
	</head>
	<body>
		<h1>I built my own web page!</h1>
		<p>A hyperlink: <a href="http://en.wikipedia.org/wiki/HTML">Here is what Wikipedia has to say about HTML</a></p>
		<p>Here is a picture of a cat:</p>
		<img src="http://upload.wikimedia.org/wikipedia/commons/4/4c/Lolcat.jpg" />
	</body>
</html>
```
That is, include the following markup just after the `<h1 />` declaration, before the `<p />` element:
```html
		<p>A hyperlink: <a href="http://en.wikipedia.org/wiki/HTML">Here is what Wikipedia has to say about HTML</a></p>
```
Hyperlinks (called 'anchors', hence the `a` element) specify not only the page or website to link to (using the `href` attribute), but also the text to display in the clickable link.

Save the file, and refresh the page in your browser. The text 'Here is what Wikipedia has to say about HTML' should now appear just after the heading, and if you click the link, it should take you to a Wikipedia page on HTML.

(12) View Source again
----------------------
In your web browser, go to http://www.wikipedia.org/ again (or any other website you know of), and 'view source' - you should now recognise some of the markup commands which are contained in the page.


(13) What have we learnt?
-------------------------
We have looked a the HTML 'source code' used to tell web browsers how to display a page - this is simply text, in HTML.

We have built up a web page step-by-step, adding:
* title
* heading
* text and image
* styles
* hyperlink

It's important to understand that the file we have created is stored only on our local computer at the moment. If we wanted to make this available publically on a website, we'd need to upload it to a server which is publically accessible.
