# simple-website

## Unit 3 of 7

Exercise - Add basic HTML to your web app
Completed
100 XP
10 minutes
At the moment, your website has an empty HTML file. Let's add some code! The goal is to use hypertext markup language (HTML) to describe the web page your customers' browsers should display. Wouldn't it be nice to have a starting template? Editors can conveniently fill in some of the typical boilerplate or HTML structure for you.

In this unit, you add basic HTML content, open the HTML page in a browser, and get your first look at the developer tools.

Add some HTML code
Visual Studio Code provides basic support for HTML programming out of the box. There's syntax highlighting, smart completions with IntelliSense, and customizable formatting.

Open your website in Visual Studio Code, then open the index.html file by selecting the index.html file in Explorer.

In the index.html page, type html:5, and then select Enter. HTML5 template code is added to the file.

 Note

If the HTML5 template code is not added to the index.html file, try closing and reopening the file.

Edit your code so that it resembles the following. Then save the file by selecting Control+S on Windows or Command+S on macOS.

HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>

</body>
</html>
```

There have been different versions of HTML. The doctype `<!DOCTYPE html> indicates this HTML document contains HTML5 code.

While we aren't going to delve deeply into the meaning of all the HTML elements, we'll point out a few important items. The meta tag indicates metadata information that won't typically be visible to the viewer unless they view the source code in their browser. Meta elements or tags provide descriptive information about the webpage. For example, they help search engines process which information in your webpages to return in search results.

The character set (charset) for UTF-8 may seem insignificant, but is crucial for establishing how computers interpret characters. If the metadata for the character set is missing, that can lead to compromised security. There's quite a bit of history and technical information behind the charset attribute, but important takeaway from this exercise is that the VS Code boilerplate provides some sensible defaults.

Edit the head

The `<head> element in your HTML code contains information about your website not visible inside the browser tab.

The metadata defines data about the HTML document, such as character set, scripts, and which browser the webpage opens in.

The title of a webpage appears at the top of a browser window, and is significant in many ways. For example, the title is used by and displayed in search engines. Let's add a title.

 Important

From this point forward, the ellipsis (```) indicates that previously declared code precedes or follows. There should be enough code provided as context to make necessary changes or update your work, but you should not  and paste the ellipsis into your code.

In the editor, modify the `<title> element so that it resembles the following example.

```html
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Simple website</title>
```

To apply styles to the HTML elements on the webpage, you could write the CSS code directly in the head of the webpage. Writing CSS in the HTML page is called internal CSS. However, it's a best practice to separate HTML structure and CSS styling. Having a separate CSS page is called external CSS. Code tends to be easier to read when it's concise and compartmentalized. You can use one or more external style sheets to service multiple webpages. Rather than updating each HTML page with replicated CSS code, you can make changes to a single CSS file, and have those updates applied to all of the dependent web pages. Let's link to an external stylesheet.

In the VS Code editor, add a blank line after the <title> element, type link, and then select Enter. VS Code should add the following line to your index.html file.

HTML

```html
<link rel="stylesheet" href="">
```

Update the href= to href="main.css", and save the file by selecting Control+S on Windows or Command+S on macOS.

HTML

```html
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Task List</title>
  <link rel="stylesheet" href="main.css">
</head>
```

Edit the body

Let's start filling in the `<body> element now.

The `<body> element contains the content of your website visible to your customers in their browsers.

Add a heading `<h1> element, followed by a paragraph `<p> element, and then create an unordered list `<ul> that contains several list item `<li> elements.

Edit your code, or  and paste, so it looks like the following example.

HTML

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple website</title>
    <link rel="stylesheet" href="main.css">
  </head>
  <body>
    <h1>Task List</h1>
    <p id="msg">Current tasks:</p>
    <ul>
      <li class="list">Add visual styles</li>
      <li class="list">Add light and dark themes</li>
      <li>Enable switching the theme</li>
    </ul>
  </body>
</html>
```

An ID attribute (used in the `<p> element) can be used for styling one element, while the class attribute (used in the `<li> element) is for styling all elements of the same class.

Before the next step, make sure your file is saved by selecting Control+S or Command+S.

Open in browser

You can preview your webpage locally by opening the HTML file in a browser. Instead of a website address that begins with https://, your browser points to the local file path, which should look similar to C:/dev/simple-website/index.html.

To preview using Visual Studio Code, right-click index.html, and select Open In Default Browser, or select the index.html file and use the keyboard shortcut Alt+B.

Screenshot of the Open in Browser context menu item in Visual Studio Code.

 Important

If you're having trouble, make sure you're directly right-clicking the filename icon or text. If a Visual Studio Code dialog appears, select Yes, I trust the authors; this is the Workspace Trust feature that lets you decide whether your project folders should allow or restrict automatic code execution. You just created the file, so it's safe.

The webpage opens in your default browser.

View the page using developer tools
You can inspect a webpage by using the developer tools in your browser. Let's give it a try.

Open Developer Tools by right-clicking in the web page and selecting Inspect, or try these shortcuts:

Press the keyboard shortcut for Developer Tools, which is F12.

Press `Ctrl+Shift+I` on Windows and Linux or `Option+Command+I` on a Mac.

These keyboard shortcuts work in Microsoft Edge, Chrome, and Firefox. If you're using Safari, see the Web Development Tools. When installed, select Safari > Preferences, and then select Advanced. At the bottom of the pane, select the Show Develop menu in menu bar checkbox. Select Develop > Show Web Inspector. For more information, check the Safari Web Inspector documentation.

To learn more about opening Developer Tools and the main available features, check out the Overview of DevTools article.

Select the Elements tab.

Screenshot showing a browser window with the website, and the Developer Tools next to it with the Elements tab selected.

Move your mouse over the HTML elements displayed in the Elements tab, and expand the contents of the various elements.

The Elements tab in developer tools shows you the document object model (DOM) as rendered in the browser. When debugging, it's often important to see how the browser interprets your source code.

Inspecting the page in a browser provides all sorts of useful information and can help you troubleshoot problems. You can also view CSS details with the inspector, as you'll see in the next section.

Next unit: Exercise - Style your HTML with CSS

## Unit 4 of 7

Cascading Style Sheets (CSS) let you specify how your page should look. The basic idea is to define what the style should be for the elements that you use within your HTML pages. While the HTML elements define your content, CSS styles define what this content looks like.

For example, you can apply rounded corners or give a gradient background to an element. Or you can use CSS to specify how hyperlinks look and respond when you interact with them. You can also perform sophisticated page layouts and animation effects.

You can apply styles to specific elements, all elements of a specific type, or use classes to style many different elements.

In this exercise, you'll apply CSS styles to HTML page elements and add some CSS code to define your light and dark themes. You'll also check the results in your browser's developer tools.

External CSS
In the previous unit about HTML, you linked to an external CSS file from HTML.

```html
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Task Timeline</title>
  <link rel="stylesheet" href="main.css">
```

One benefit of external CSS is that multiple HTML pages can link to the same CSS file. If you make a change to the CSS, your styling will update for each page. Using an HTML file for your page content, a CSS file for styling, and a JavaScript file for interaction is called separation of concerns.

As described previously, you can also write CSS directly in HTML, which is called internal CSS. Even for a basic website, there are so many CSS rules the HTML page can become cluttered quickly. With more than one page, the same CSS would often be repeated and challenging to manage.

CSS rules
CSS rules are how you apply styles to HTML elements. CSS rules have a selector which is used to express which element, or elements, should the styles be applied to.

In Visual Studio Code, open the main.css file, and enter the following.

css

```css
body {
    font-family: monospace;
}

ul {
    font-family: helvetica;
}
```

The above code snippet contains two rules. Each rule has:

A selector. body and ul are the selectors of the two rules and are used to select which element(s) the styles apply to.
An opening curly brace ({).
A list of style declarations that determine what the selected elements should look like.
A closing curly brace (}).
For example, the ul selector selects the `<ul> HTML element in the page, to apply styles to it. The declaration is `font-family: helvetica` and determines what the style should be. The property name is `font-family`, and the value is `helvetica`.

As you'll see next, you can define your own custom names for elements.

## Selectors

ID and class selectors enable you to apply styles to custom attribute names in your HTML. An ID is used to style one element, whereas classes can be used to style multiple elements.

Copy the following code into your CSS file, after the closing curly brace for ul selector that you added previously.

css

```css
li {
  list-style: circle;
}

.list {
  list-style: square;
}

#msg {
  font-family: monospace;
}
```
The preceding code contains three CSS rules, with the last two rules using custom attributes to select elements: .list and #msg.

.list is a class selector. Each HTML element that contains a class attribute set to list will get the styles that are defined within this selector.

#msg is an ID selector. The HTML element that has its id attribute set to msg will get the styles that are defined within this selector.

The names that you use for your selectors can be arbitrary, as long as they match what you've defined in the HTML.

Save your work by selecting Control+S on Windows or Command+S on macOS.

View in browser

To preview using VS Code, right-click the file name index.html, and then select Open In Default Browser.

 Important

Even though you were just editing the main.css file, to preview the changes, you should select the index.html file.

The webpage opens in your default browser.

Screenshot of the website with the font styles applied.

Are the font styles what you expected to see? It's interesting how styles applied to the `<body> are inherited on the `<h1> element. We didn't define anything for `<h1>, but it still got the font that was defined on `<body>. This inheritance mechanism from parent elements to their descendants is one of the key aspects of CSS. However, the `<li> elements have a different font, overriding the one set on `<body> because they're also descendants of the `<ul> element which you defined a style for.

Note that using Open In Default Browser in VS Code opens a new tab in the browser every time. To avoid opening a new tab, you can reload the tab that already contains your website instead.

To reload the tab press F5, which is the refresh keyboard shortcut, or press Ctrl+R on Windows or Linux, and Command+R on a Mac.

Add a light theme
Next, you'll add support for a color theme for your website. Begin by defining a light-colored theme using hex color codes.

In your CSS file, add the following code at the end of the file.

css

```css
.light-theme {
  color: #000000;
  background: #00FF00;
}
```
In this example, #000000 specifies black for the font color, and #00FF00 specifies green for the background color.

In your HTML file, update the `<body> element with a class name, light-theme, so the class selector for light theme will apply the styles correctly.

HTML

```html
<body class="light-theme">
```

View in browser

To preview using Visual Studio Code, right-click index.html, and then select Open In Default Browser or reload the previous tab by pressing F5.

Notice that the light theme using a green background appears.

Screenshot of the website with its light theme applied.

View applied CSS
On the browser view, open Developer Tools.

Right click the page and select Inspect, or select the shortcut F12 or Ctrl-Shift+I.

Select the Elements tab and, inside the Elements tab, select the Styles tab (it should already be selected by default).

Hover over the various HTML elements, and as you select a few elements, notice how the developer tools display which styles are applied to them in the Styles tab.

Select the `<body> element. Note the light-theme applied.

Select the unordered list `<ul> element. Note the custom style font-family: helvetica;, which overrides the style for the `<body> element.

Screenshot of the website with its light theme applied and the Developer Tools next to it showing the Elements panel with the HTML and CSS code.

To learn more about viewing CSS styles in Developer Tools, check out the Get started viewing and changing CSS article.

Add a dark theme
For the dark theme, you'll set up the infrastructure in preparation for the next unit, in which you'll enable theme switching on the web page.

To add support for a dark theme to your CSS, use the following steps.

Add some constants to the page root at the top of your CSS file.

css

```css
:root {
  --green: #00FF00;
  --white: #FFFFFF;
  --black: #000000;
}
```

The `:root` selector represents the `<html> element in the HTML page. For this kind of task, a best practice is to define a set of global CSS variables in a CSS rule with the :root selector. In this example, you've defined three color variables. You'll next be able to use these variables in other CSS rules.

At the end of the CSS file, replace the light-theme rule with the following code to update it and to add the dark-theme selector.

css

```css
.light-theme {
  --bg: var(--green);
  --fontColor: var(--black);
}
.dark-theme {
  --bg: var(--black);
  --fontColor: var(--green);
}
```

In the preceding code, you defined two new variables, bg and fontColor, which specify a background and font color. These variables use the var keyword to set their property values to the variables previously specified in your :root selector.

Next, in your CSS file, replace the current body selector with the following code.

css

```css
body {
  background: var(--bg);
  color: var(--fontColor);
  font-family: helvetica;
}
```

In this example, you use the body selector to set the background and color properties and, because the elements that are visible on the web page are all inside the `<body> element, they'll inherit the colors set on `<body>.

In your CSS file, remove the rules with the #msg and ul selectors so that they also inherit the same font from `<body>.

To view the dark theme, open the file index.html and manually edit the default theme in the `<body> class attribute to dark theme (dark-theme), and then reload the page in the browser.

Screenshot of the website with its dark theme applied and the Developer Tools next to it.

Edit the `<body> class attribute to switch the default back to light theme.

In the next unit, you'll use JavaScript to provide interactivity and support the switching of themes.

Next unit: Exercise - Add interactivity with JavaScript

## Unit 5 of 7

Exercise - Add interactivity with JavaScript

JavaScript (or ECMAScript) is a programming language that helps you add interactivity to your web pages.

For example, you can use JavaScript to define the behavior that will happen when a user selects a button; for example, open a pop-up window. Using JavaScript, you can add or remove content from a web page without reloading it.

In this unit, you'll set up an example JavaScript file for your web page. You'll create a button to switch between light and dark themes. Then you'll attach the button to JavaScript code that performs the actual theme switching. Finally, you'll check the finished project using your browser's developer tools.

Link to JavaScript
Like CSS, you could add JavaScript directly to the HTML file, but a recommended best practice is to save your JavaScript in a separate file. Adding your JavaScript code to a separate file makes it easier to reuse it across several web pages. For example, you could create a pop-up alert by adding `<script>alert('Hello World')</script>` anywhere within the body of your web pages; however, it's better to add your JavaScript code to a separate file that can be linked to every file that needs your custom functionality.

The HTML script tag `<script>` will let us link to an external JavaScript file, which is how you'll configure your web app in this exercise.

In VS Code, open your `index.html` file.

On a new line before the closing `</body>` element, enter script:src, and then select Enter. The opening and closing tags for a script are added to your code.

Modify the `<script>` element to load your app.js file as shown in the following example, and ensure that it's located after the closing `</ul>` element for the list.

HTML


```html
<ul>
  <li class="list">Add visual styles</li>
  <li class="list">Add light and dark themes</li>
  <li>Enable switching the theme</li>
</ul>
<script src="app.js"></script>
```

The `<script>` element could be placed in the `<head> or elsewhere in the `<body>. However, putting `<script> element at the end of the `<body> section enables all the page content to display on the screen first, and then load the script.

Add fault tolerance
In your HTML file, add a `<noscript> element after the closing `</script> tag, which can be used to show a message if JavaScript is deactivated.

HTML

```html
<script src="app.js"></script>
<noscript>You need to enable JavaScript to view the full site.</noscript>
```

Adding the `<noscript> element is an example of fault tolerance or graceful degradation. By using the `<noscript> element, your code can detect and plan for when a feature isn't supported or available.

Save your changes with the keyboard shortcut Control+S on Windows or Command+S on macOS.

Set strict mode
JavaScript was designed to be easy to learn and allows certain mistakes to be made by the developer. For example, JavaScript does not throw an error when you use a misspelled variable, and instead creates a new global one. While having fewer errors is tempting when you start learning JavaScript, it can lead to writing code that is harder for browsers to optimize and harder for you to debug.

Switch to strict mode to get more useful errors when you make mistakes.

In VS Code, open the app.js file, and enter the following.

JavaScript

```js
'use strict';
```

Add a button

You need a way to let your users switch between the light and dark themes in your web page. In this exercise, you'll implement that functionality with an HTML `<button> element.

In your HTML file, add a `<button> element. Put the button at the end of the list inside of a `<div> element.

```html
<ul>
  <li class="list">Add visual styles</li>
  <li class="list">Add light and dark themes</li>
  <li>Enable switching the theme</li>
</ul>
<div>
  <button class="btn">Dark</button>
</div>
<script src="app.js"></script>
```

Notice that the <button> element in this example has a class attribute that you'll use to apply CSS styles.

In your CSS file, add a new rule with a .btn class selector for your HTML button. To make the button colors different from the general light or dark theme colors, set the color and background-color properties in this rule. They'll override the default ones set in the body rule of your CSS file.

```css
.btn {
  color: var(--btnFontColor);
  background-color: var(--btnBg);
}
```

Next, modify the .btn rule to add some styles for the size, shape, appearance, and placement of the button. The following CSS creates a round button to the right of the page heading.

```css
.btn {
  position: absolute;
  top: 20px;
  left: 250px;
  height: 50px;
  width: 50px;
  border-radius: 50%;
  border: none;
  color: var(--btnFontColor);
  background-color: var(--btnBg);
}
```

Next, update the CSS for the light and dark theme. Define some new variables, --btnBg and --btnFontColor, to specify the button-specific background color and font color.

```css
.light-theme {
  --bg: var(--green);
  --fontColor: var(--black);
  --btnBg: var(--black);
  --btnFontColor: var(--white);
}
.dark-theme {
  --bg: var(--black);
  --fontColor: var(--green);
  --btnBg: var(--white);
  --btnFontColor: var(--black);
}
```

Add an event handler

To make the button do something when you select it, you need an event handler in your JavaScript file. An event handler is a way to run a JavaScript function when an event happened on the page. For the button, let's add an event handler for the click event; the event handler function runs when the click event occurs.

Before you can add the event handler, you need a reference to the button element.

In your JavaScript file, use document.querySelector to get the button reference.

JavaScript

```js
const switcher = document.querySelector('.btn');
```

The `document.querySelector` function uses CSS selectors, just like the ones you used in your CSS file. switcher is now a reference to the button in the page.

Next, add the event handler for the click event. In the following code, you add a listener for the click event and define an event handler function to be executed by the browser when the click event occurs.

JavaScript

```js
switcher.addEventListener('click', function() {
    document.body.classList.toggle('light-theme');
    document.body.classList.toggle('dark-theme');
});
```

In the preceding code, you used the toggle method to modify the `<body> element's class attribute. This method automatically adds or removes the light-theme and dark-theme classes. This code applies the dark styles instead of light styles on click, and then light styles instead of dark if you click again.

However, the label for the button also needs to be updated to show the correct theme, so you need to add an if statement to determine the current theme, and update the button label.

Here's what the complete JavaScript code should look like.

JavaScript

```js
'use strict';

const switcher = document.querySelector('.btn');

switcher.addEventListener('click', function() {
    document.body.classList.toggle('light-theme');
    document.body.classList.toggle('dark-theme');

    const className = document.body.className;
    if(className == "light-theme") {
        this.textContent = "Dark";
    } else {
        this.textContent = "Light";
    }
});
```

It's a JavaScript convention to use camel case for variable names with more than one word; for example: the variable className.

Console message

As a web developer, you can create hidden messages that won't appear on your webpage, but that you can read in the Developer Tools, in the Console tab. Using console messages is helpful for seeing the result of your code.

Add a call to `console.log` after the if statement, but inside the event listener.

JavaScript

```js
switcher.addEventListener('click', function() {
    document.body.classList.toggle('light-theme');
    document.body.classList.toggle('dark-theme');

    const className = document.body.className;
    if(className == "light-theme") {
        this.textContent = "Dark";
    } else {
        this.textContent = "Light";
    }

    console.log('current class name: ' + className);
});
```

In VS Code, when in a JavaScript file, you can use autocomplete for console.log by entering log, and then pressing Enter.

You can define a text string with single or double quotes around the text.

Open in the browser

To preview, select `index.html`, and select Open In Default Browser, or reload the same browser tab by pressing `F5`.

Screenshot of the website showing the new button.

Select the new Dark button to switch to the dark theme.

Screenshot of the website after switching to dark theme.

Make sure that everything looks correct and behaves as expected. If not, you should review the preceding steps to see if you missed something

Check the page in the developer tools
Open Developer Tools.

Right-click and select Inspect, or use the keyboard shortcut F12. Alternatively, use the Ctrl+Shift+I shortcut on Windows or Linux, and Option+Command+I on macOS.
Select the Elements tab and, inside the Elements tab, select the Styles tab.

Select the `<body> element. In the Styles tab, look at the applied theme. If the current theme is dark, the dark-theme styles are applied.

Make sure the dark theme is selected.

Select the Console tab to see the console.log message, current class name: dark-theme.

Screenshot of the browser window with the website and the Developer Tools console open showing the console  message.

Using the console, you can get interesting insights from your JavaScript code. Add more console messages to understand which parts of your code are getting executed and to know the current values of other variables.

## Summary

In this module, you set up a working environment for web development. You also created a website and tested that everything is working in a web browser.

You downloaded and installed the tools you need for web development, and customized the editor with basic packages.
You created a project directory and the files to build a website.
You created a heading and other page elements, and then linked to external files and tested the page in a browser.
You applied styles to different elements and tested your site in the browser, and added support for themes using CSS.
You added JavaScript to enable custom interaction with the page and switching between themes.
You learned how to create and use console messages to peek inside your code.
You're gathering tools and building a foundation as a web developer. You can reuse your website as a template for future projects. As your skills and knowledge grow, you'll be able to fulfill more of the vision you have for your website. It's also empowering to see an idea come to life.
