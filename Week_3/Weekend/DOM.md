# DOM

Document Object Model (DOM) is created by the browser when the page is loaded to represent all of the HTML code on that page.

HTML --> `document` object (DOM)
- converts the html content and elements to tree structure of objects

DOM allows programming language to manipulate the content, structure and style of the website
- Any action on website like slideshows, click of button, toggling menu etc are a **result of JS manipulating the DOM**

## **What is DOM?**

named `document` and each element is an object similar to object structure in JS
- has **properties** and **methods**

You can use client-side JS to edit/alter HTML elements but this only alters the code in the browser and not the source code

DOM is a tree structure, so each item is a node
- the **document** itself is also a node which is the root of that tree

Tha main ones are:
- element nodes  -->  refers to html element (`<body>`, `<div>`, etc)
- text nodes     -->  text that is not part of element 
- comment nodes  -->  `<!-- HTML comment -->`



