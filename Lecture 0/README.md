# Lecture 0

- HTML is a markup language that defines the structure of a web page. It is interpreted by your web browser (Safari, Google Chrome, Firefox, etc.) in order to display content on your screen.
- Let’s get started by writing a simple HTML file!

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Hello!</title>
    </head>
    <body>
        Hello, world!
    </body>
<html>
```

When we open up this file in our browser, we get:

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled.png)

Now, let’s take some time to talk about the file we just wrote, which seems to be pretty complicated for such a simple page.

- In the first line, we are declaring (to the web browser) that we are writing the document in the latest version of HTML: HTML5.
- After that, the page consists of nested **HTML elements** (such as html and body), each with an **opening and closing tag** marked with either `<element>` for an opening and `</element>` for a closing.
- Notice how each of the inner elements is indented just a bit further than the last. While this is not necessarily required by the browser, it will be very helpful to keep this up in your own code.
- HTML elements can include **attributes**, which give the browser extra information about the element. For example, when we include `lang="en"` in our initial tag, we are telling the browser that we are using English as our primary language.
- Inside the HTML element, we typically want to include both a `head` and a `body` tag. The head element will include information about your page that is not necessarily displayed, and the body element will contain what is actually visible to users who visit the site.
- Within the head, we have included a `title` for our webpage, which you’ll notice is displayed in the tab at the top of our web browser.
- Finally, we’ve included the text “Hello, world!” in the body, which is the visible part of our page.

**Document Object Model (DOM)**

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%201.png)

The DOM is a convenient way of visualizing the way HTML elements relate to each other using a tree-like structure. Above is an example of the DOM layout for the page we just wrote.

**More HTML Elements**

- There are many HTML elements you may want to use to customize your page, including headings, lists, and bolded sections. In this next example, we’ll see a few of of these in action.
- One more thing to note: `<!-- -->` gives us a comment in HTML, so we’ll use that below to explain some of the elements.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>HTML Elements</title>
    </head>
    <body>
        <!-- We can create headings using h1 through h6 as tags. -->
        <h1>A Large Heading</h1>
        <h2>A Smaller Heading</h2>
        <h6>The Smallest Heading</h6>

        <!-- The strong and i tags give us bold and italics respectively. -->
        A <strong>bold</strong> word and an <i>italicized</i> word!

        <!-- We can link to another page (such as cs50's page) using a. -->
        View the <a href="https://cs50.harvard.edu/">CS50 Website</a>!

        <!-- We used ul for an unordered list and ol for an ordered one. both ordered and unordered lists contain li, or list items. -->
        An unordered list:
        <ul>
            <li>foo</li>
            <li>bar</li>
            <li>baz</li>
        </ul>
        An ordered list:
        <ol>
            <li>foo</li>
            <li>bar</li>
            <li>baz</li>
        </ol>

        <!-- Images require a src attribute, which can be either the path to a file on your computer or the link to an image online. It also includes an alt attribute, which gives a description in case the image can't be loaded. -->
        An image:
        <img src="../../images/duck.jpeg" alt="Rubber Duck Picture">
        <!-- We can also see above that for some elements that don't contain other ones, closing tags are not necessary. -->

        <!-- Here, we use a br tag to add white space to the page. -->
        <br/> <br/>

        <!-- A few different tags are necessary to create a table. -->
        <table>
            <thead>
                <th>Ocean</th>
                <th>Average Depth</th>
                <th>Maximum Depth</th>
            </thead>
            <tbody>
                <tr>
                    <td>Pacific</td>
                    <td>4280 m</td>
                    <td>10911 m</td>
                </tr>
                <tr>
                    <td>Atlantic</td>
                    <td>3646 m</td>
                    <td>8486 m</td>
                </tr>
            </tbody>
        </table>
    </body>
<html>
```

This page, when rendered, looks something like this:

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%202.png)

- In case you’re worried about it, know that you’ll never have to memorize these elements. It’s very easy to simply search something like “image in HTML” to find the `img` tag. One resource that’s especially helpful for learning about these elements is [W3 Schools](https://www.w3schools.com/html/html_elements.asp).

### **Forms**

- Another set of elements that is really important when creating a website is how to collect information from users. You can allow users to enter information using an HTML form, which can contain several different types of input. Later in the course, we’ll learn about how to handle information once a form has been submitted.
- Just as with other HTML elements, there’s no need to memorize these, and W3 Schools is a great resource for learning about them!

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Forms</title>
</head>
<body>
    <form>
        <input type="text" placeholder="First Name" name="first">
        <input type="password" placeholder="Password" name="password">
        <div>
            Favorite Color:
            <input name="color" type="radio" value="blue"> Blue
            <input name="color" type="radio" value="green"> Green
            <input name="color" type="radio" value="yellow"> Yellow
            <input name="color" type="radio" value="red"> Red

        </div>
        <input type="submit">
    </form>
</body>
</html>
```

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%203.png)

**CSS (Cascading Style Sheets)**

- CSS is used to customize the appearance of a website.
- While we’re just getting, started, we can add a style attribute to any HTML element in order to apply some CSS to it.
- We change style by altering the CSS properties of an element, writing something like `color: blue` or `text-align: center`
- In this example below, we make a slight change to our very first file to give it a colorful heading:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Hello!</title>
    </head>
    <body>
        <h1 style="color: blue; text-align: center;">A Colorful Heading!</h1>
        Hello, world!
    </body>
<html>
```

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%204.png)

If we style an outer element, all of the inner elements automatically take on that style. We can see this if we move the styling we just applied from the header tag to the body tag:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Hello!</title>
    </head>
    <body style="color: blue; text-align: center;">
        <h1 >A Colorful Heading!</h1>
        Hello, world!
    </body>
<html>
```

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%205.png)

While we can style our web page as we’ve done above, to achieve better design, we should be able to move our styling away from the individual lines.

- One way of doing this is to add your styling between `<style>` tags in the `head`. Inside these tags, we write which types of elements we want to be style, and the styling we wish to apply to them. For example:

```html
<html lang="en">
  <!DOCTYPE html>
  <head>
      <title>Hello!</title>
      <style>
          h1 {
              color: blue;
              text-align: center;
          }
      </style>
  </head>
  <body>
      <h1 >A Colorful Heading!</h1>
      Hello, world!
  </body>
  </html>
```

Another way is to include in a `<link>` element in your `head` with a link to a styles.css file that contains some styling. This means the HTML file would look like:

```html
<html lang="en">
  <!DOCTYPE html>
  <head>
      <title>Hello!</title>
      <link rel="stylesheet" href="styles.css">
  </head>
  <body>
      <h1 >A Colorful Heading!</h1>
      Hello, world!
  </body>
  </html>
```

And our file called `styles.css` would look like:

```css
h1 {
      color: blue;
      text-align: center;
  }
```

- There are far too many CSS properties to go over here, but just like HTML elements, it’s typically easy to Google something along the lines of “change font to blue CSS” to get the result. Some of the most common ones though are:
    - `color`: the color of text
    - `text-align`: where elements are placed on the page
    - `background-color`: can be set to any color
    - `width`: in pixels or percent of a page
    - `height`: in pixels or percent of a page
    - `padding`: how much space should be left inside an element
    - `margin`: how much space should be left outside an element
    - `font-family`: type of font for text on page
    - `font-size`: in pixels
    - `border`: size type (solid, dashed, etc) color
- Let’s use some of what we just learned to improve upon our oceans table from above. Here’s some HTML to start us off:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Nicer Table</title>
    </head>
    <body>
        <table>
            <thead>
                <th>Ocean</th>
                <th>Average Depth</th>
                <th>Maximum Depth</th>
            </thead>
            <tbody>
                <tr>
                    <td>Pacific</td>
                    <td>4280 m</td>
                    <td>10911 m</td>
                </tr>
                <tr>
                    <td>Atlantic</td>
                    <td>3646 m</td>
                    <td>8486 m</td>
                </tr>
            </tbody>
        </table>
    </body>
<html>
```

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%206.png)

The above looks a lot like what we had before, but now, either by including a `style` tag or a `link` to a stylesheet in the head element, we add the following css:

```css
table {
    border: 1px solid black;
    border-collapse: collapse;
}

td {
    border: 1px solid black;
    padding: 2px;
}

th {
    border: 1px solid black;
    padding: 2px;
}
```

Which leaves us with this nicer-looking table:

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%207.png)

You may already be thinking that there’s some needless repetition in our CSS at the moment, as `td` and `th` have the same styling. We can (and should) condense this down to the following code, using a comma to show the styling should apply to more than one element type.

```css
table {
    border: 1px solid black;
    border-collapse: collapse;
}

td, th {
    border: 1px solid black;
    padding: 2px;
}
```

- This is a good introduction into what are known as [CSS selectors](https://www.w3schools.com/cssref/css_selectors.asp). There are many ways to determine which HTML elements you are styling, some of which we’ll mention here:
    - **element type**: this is what we’ve been doing so far: styling all elements of the same type.
    - **id**: Another option is to give our HTML elements an id like so: `<h1 id="first-header">Hello!</h1>` and then applying styling using `#first-header{...}` using the hashtag to show that we’re searching by id. Importantly, no two elements can have the same id, and no element can have more than one id.
    - **class**: This is similar to id, but a class can be shared by more than one element, and a single element can have more than one class. We add classes to an HTML element like this: `<h1 class="page-text muted">Hello!</h1>` (note that we just added two classes to the element: `page-text` and `muted`). We then style based on class using a period instead of a hashtag: `.muted {...}`
- Now, we also have to deal with the problem of potentially conflicting CSS. What happens when a header should be red based on its class but blue based on its id? CSS has a specificity order that goes:
    1. In-line styling
    2. id
    3. class
    4. element type
- In addition to the comma for multiple selectors, there are several other ways to specify which elements you would like to style. This table from lecture provides a few, and we’ll go through a few examples below:

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%208.png)

**Descendant Selector**: Here, we use the descendant selector to only apply styling to list items found within an unordered list:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Using Selectors</title>
        <style>
            ul li {
                color: blue;
            }
        </style>
    </head>
    <body>
        <ol>
            <li>foo</li>
            <li> bar
                <ul>
                    <li>hello</li>
                    <li>goodbye</li>
                    <li>hello</li>
                </ul>
            </li>
            <li>baz</li>
        </ol>

    </body>
<html>
```

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%209.png)

**Attributes as Selectors**: We can also narrow down our selection based on the attributes we assign to HTML elements using brackets. For example, in the following list of links, we choose to only make the link to Amazon red:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Using Selectors</title>
        <style>
            a[href="https://www.amazon.com/"] {
                color: red;
            }
        </style>
    </head>
    <body>
        <ol>
            <li><a href="https://www.google.com/">Google</a></li>
            <li><a href="https://www.amazon.com/">Amazon</a> </li>
            <li><a href="https://www.facebook.com/">Facebook</a></li>
        </ol>

    </body>
<html>
```

![Untitled](Lecture%200%202398c50e72e047ee96765e3622899cf6/Untitled%2010.png)

- Not only can we use CSS to change what an element looks like permanently, but also what it looks like under certain conditions. For example, what if we wanted a button to change color when we hover over it? We can acheive this using a [CSS pseudoclass](https://www.w3schools.com/css/css_pseudo_classes.asp), which provides additional styling during special circumstances. We write this by adding a colon after our selector, and then adding the circumstance after that colon.
- In the case of the button, we would add `:hover` to the button selector to specify the design only when hovering:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Pseudoclasses</title>
        <style>
            button {
                background-color: red;
                width: 200px;
                height: 50px;
                font-size: 24px;
            }

            button:hover {
                background-color: green;
            }
        </style>
    </head>
    <body>
        <button>Button 1</button>
        <button>Button 2</button>
        <button>Button 3</button>

    </body>
<html>
```