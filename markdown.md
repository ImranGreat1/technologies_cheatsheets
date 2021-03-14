# What is markdown

Markdown is a lightweight markup language with a plain text formatting syntax.
Markdown can be converted into HTML/XHTML and other formats.
Markdown's main purposes is readability and ease of use.

## Uses of markdown

Mainly ReadMe files such as in github and other platforms
Used in forum and blog post
Used in many static site generators

## Some of the things you can format with mackdown

Headings
Lists
Emphasis
Links
Images
Blocks of Code
Blockquotes
Horizontal Rules

## Markdown Cheatsheet

<!-- Headings -->

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

<!-- Italic -->

*This text* is Italic

_This text_ is Italic

<!-- Strong -->

**This text** is Bold

__This text__ is Bold

<!-- Strikethrough -->

~~This text~~ is strikethrough

<!-- Horizontal Rule -->
___
---

<!-- Esacping a special character -->
\*This text\* is Italic


<!-- Blockquote -->
> This is a blockquote

<!-- Links -->
[Google Search](www.google.com)
<!-- Links with title -->
[Google Search](www.google.com "Search Anything")


<!-- Unordered List -->
* Item 1
* Item 2
* Item 3
    * Nested Item 1
    * Nested Item 2
* Item 4


<!-- Ordered List -->
1. Item 1
1. Item 2
1. Item 3


<!-- Inline Code Block -->
`<p>This is an Inline Code Block</p>`


<!-- Image -->
![Markdown Image](https://markdown-here.com/img/icon256.png)



<!-- GITHUB MARKDOWN -->

<!-- Code Blocks -->
<!-- bash, javascript and python header tell github the  type of code that was written in it so that githug should nicely format the code base on the language -->
```bash
    npm install
    
    npm start
```

```javascript
    function add(num1, num2) {
        return num1 + num2;
    }
```

```python
    def add(num1, num2):
        return num1 + num2
```


<!-- Table -->
| Name      | Email             |
| ----------| ------------------|
| John Doe  | john@example.com  |
| Jane Doe  | jane@example.com  |


<!-- Task List -->
* [x] Task 1
* [x] Task 2
* [ ] Task 3