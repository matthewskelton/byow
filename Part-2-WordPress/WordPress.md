Build Your Own Website - Part 2 - WordPress
===========================================

Synopsis
--------
In this part, we'll register for a WordPress blog website, create some pages, and see how HTML is used by WordPress to create pages.

*Screenshots of how each step are included as WordPress-XX-Y.png, where XX is the numbered section below, and Y is the numbered bullet-point within that section.*

(1) Register for WordPress
--------------------------
We will use the popular WordPress.com platform to create a simple public website.

1. Go to http://wordpress.com/ in your browser
1. Click on Get Started --> https://signup.wordpress.com/signup/ should be the resulting page
    1. Fill in your details
1. Choose the Free plan
1. Verify your email address if necessary
1. Go to the Dashboard (My Blogs --> Blog Admin)


(2) Choose a theme
------------------
We'll now choose a theme (colour scheme) for our new website.

1. If 'Appearance' does not show in the menu on the left-hand side, click the > arrow
1. Click 'Appearance' and then 'Themes'

A variety of themese is available - pick one which you like, and which is free. You can preview the new theme before applying it by clicking 'Live Preview' underneath the theme name.

(3) Create the About and Contact pages
--------------------------------------
Now we'll create two static (fixed) pages: About and Contact. These pages are used by visitor to your website to find information on what the site is about.

1. Click on 'Pages' then 'Add New'
1. In the box just underneath 'Edit Page', type the title of the page (either 'About' or 'Contact')
1. In the edit box underneath, type some details relevant to the page. For instance, for the Contact page, add a [fictional] telephone number, email address or postal address.
	1. You can use some formatting like bold, italic, underline, hyperlinks, and headings for the text.
	1. It is best to avoid more complicated styles.
1. Click 'Preview' to see how the page will appear after it's published.
1. When you are happy with the initial version of the page, click 'Publish' (or 'Save Draft' if you want to publish later)
1. You can view the published page by clicking 'View page' - the published page will open in a new browser tab or window.


(4) Look at the page HTML
-------------------------
We will now look to see how WordPress uses HTML to create our pages. Firstly, we will look at the text we entered for our pages. We will then look at the source for the whole page to see how our text fits with the other HTML code.

1. Click on Pages --> All pages, then click 'Edit' underneath the Contact (or About) page which you just created.
1. Click the 'Text' tab to the top right of the editor. This takes us into HTML editing mode.
1. We can see that the text area now contains some HTML markup representing the visual version we have edited before. 
1. We'll now underline some text in a similar way to how we created our web page in Part 1. Find a word or sentence in the editor area and place a `<u>` before it and a `</u>` after it - this will underline the word or sentence.
1. Click the 'Visual' tab at the top right of the editor to switch back to visual mode - the word or sentence should now be underlined.

WordPress is using the same kind of HTML as we used in Part 1 to define bold, underline, and headings.

(5) View page source
-------------------
We'll now see how WordPress uses HTML to create the whole page (not just the text we were editing).

1. In your browser, view the page you created (Contact or About). This will be something like http://BLOGNAME.wordpress.com/contact/, where BLOGNAME is the name of your WordPress website.
1. Do a view source:
	1. Google Chrome: right-click on page -> View page source
	1. Internet Explorer: right-click on page -> View source
	1. Firefox: right-click on page -> View Page Source
1. Look for the HTML elements with which you are familiar:
	1. html
	1. head
	1. title
	1. body
1. Look for the text you edited in the page (such as an email address or telephone number). You should see that WordPress has used HTML to tell the browser how to display ('render') the text and formatting.

So we can see that the way which WordPress contructs whole web pages is actually the same as the method we used in Part 1, just with a larger number of HTML elements.

(6) Exploring WordPress
To expand your website, you can add a series of blog posts (see 'Posts'), or experiment with 'Widgets', small parts of the page used to show things like categories, tags, your latest Twitter updates, and many other things; see 'Appearance' --> 'Widgets'.

Just remember: underneath all the wizardy, WordPress is doing little more than creating web pages in HTML, just as you can do in a text editor!
