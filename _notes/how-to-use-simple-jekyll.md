---
title: How to use Simply Jekyll features on your website
tags: simplyjekyll
---

Welcome to this feature usage tour. This is going to be another short post that describes how to use all the fancy features we saw in [[Exploring the features of Simply Jekyll]]. So without further ado, let's get started.

## The default features

All the default jekyll markdown features are made available such that they don't cause any conflict with the custom features that we have implemented. To see how to the raw markdown gets generated, go to the [[Test page to see how the raw markdown is rendered]]

## The Custom features

### 1. Creating a wiki-style link

**<u>General Syntax</u>**

- **Internal links:** **[​[**​Some Link**]]**

- **External links:** **[​[​**Some Text::https://address-to-the-website**]]**

Anything text inside a double square bracket is considered as an internal link. The text has to be a valid title, if you provide a random text inside double square brackets, it will showup highlighted in yellow telling you that there is no essay/article/file with the mentioned title.

Similarly, for external links all you have to do is add a double colon after the "Alt text" and enter the link to the website after the double colon as seen below.

**Examples**

Example of an internal link that points to a valid post or page, that is, a page with the title (not url) mentioned in the double brackets.

> **Raw Syntax:** **[​[**​Exploring the features of Simply Jekyll**]]**
>
> **Rendered Text:** [[Exploring the features of Simply Jekyll]]


Example of an internal link that do not point to a valid post or page, that is, a page with the title (not url) mentioned in the double brackets.

> **Raw Syntax:** **[​[**Title of a non-existent page**]]**
> 
> **Rendered Text:** [[Title of a non-existent page]]

### 2. Creating a sidenote or a marginnote

**<u>General Syntax</u>**

- **Sidenote:** **[​[**Some Text**::keyword-of-the-type-of-the-sidenote]]**

- **Marginnote:** **[​[​**Some Text**::keyword-of-the-type-of-the-marginnote]]**

> |Type of the sidenote/marginnote|keyword|
  |:--|:--|
  |Left Sidenote| `lsn` |
  |Right Sidenote | `rsn` |
  |Left Marginnote| `lmn` |
  |Right Marginnote | `rmn` |


So, all you have to do is type in the keywords of the corresponding type of sidenote or marginnote after the double colon in the above syntax

**Examples**

Example of a sidenote to the right side of the page: 

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. **[​[**Phasellus mollis lectus id efficitur mollis.**::rsn]]** Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. [[Phasellus mollis lectus id efficitur mollis.::rsn]] Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.

Same goes with `lsn`, `rmn`, `lmn`

### 3. Highlighting a piece of text

**<u>General Syntax</u>**

- **[​[**​Some Link**::highlight]]**

There is only one color right now in which it highlights, a light bluish color, but you can easily extend it to support multiple colors by tinkering with it in `content.html` file in `_includes` directory.

**Examples**

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. **[​[**Phasellus mollis lectus id efficitur mollis.**::highlight]]** Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. [[Phasellus mollis lectus id efficitur mollis.::highlight]] Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.

### 4. Partial Transclusion

Transclusion is just a natural extension of sidenote and marginnote feature.

**<u>General Syntax</u>**

- **Sidenote-transclusion:** **[​[**Some Text**::keyword-of-the-type-of-the-sidenote-transclusion]]**

- **Marginnote-transclusion:** **[​[​**Some Text**::keyword-of-the-type-of-the-marginnote-transclusion]]**

> |Type of the sidenote/marginnote transclusion|keyword|
  |:--|:--|
  |Left Sidenote Transclusion | `lsn-transclude` |
  |Right Sidenote Transclusion | `rsn-transclude` |
  |Left Marginnote Transclusion | `lmn-transclude` |
  |Right Marginnote Transclusion | `rmn-transclude` |


So, all you have to do is type in the keywords of the corresponding type of sidenote or marginnote after the double colon in the above syntax

**Examples**

Example of a transclusion to the right side of the page: 

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. **[​[**Exploring the features of Simply Jekyll**::rmn-transclude]]** Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. [[Exploring the features of Simply Jekyll::rmn-transclude]] Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.

Same goes with `rsn`, `lsn`, `lmn`

### 5. Wrapping a text inside a box

_Note: I've updated the `<blockquote>` to have the box by default_

**<u>General Syntax</u>**

- **[​[**Some Text**::wrap]]**

**Examples**

> **Raw Syntax:** **[​[**Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis**::wrap]]**.
>
> **Rendered Text:** [[Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.::wrap]]

### 6. Flashcard

**<u>General Syntax</u>**

- **[​[**Some Text**::srs]]**

**Examples**

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. **[​[**Donec rutrum tortor in pharetra vehicula**::srs]]**. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. [[Donec rutrum tortor in pharetra vehicula::srs]]. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.

### 7. Specific classes for changing font-type, font-size, and font-weight

_Note: This is something that [[Kramdown]] supports, but [[CommonMark]] does not. This means HTML syntax will be needed and that none of the examples below will render_

There are classes like very-small, medium-small, small, small-medium, medium, medium-large, large, very-large; that can be used to change the size of your text directly from markdown like this:

> **Raw Syntax:**
> {:.regular-sans}
> ```
> {:.large}
> Some text here that needs to be enlarged
> ```
>
> **Rendered Text:**
> 
> 
> <p class="large">Some text here that needs to be enlarged</p>


Similarly there are classes like regular-sans, serif, bold, italic, oblique, bolder, etc for formatting the text.

> **Raw Syntax:**
> 
> ```
> {:.medium .serif .oblique}
> Some text here that needs to be enlarged
> ```
>
> **Rendered Text:**
> 
> {:.medium .serif .oblique}
> Some text here that needs to be enlarged

Other common classes are `.boxit` that is used to wrap the text, `.disable-user-select` to disallow users from being able to select a particular piece of text by selecting it, etc. There are more classes like these which you can see in the file `style.css`. Once you figure out which class to use, all you have to do is just add the class before the text you want inside a curl brace like this ​{:\<classnames-with-dot-prepended-to-them>​}
 
### 8. Other implicit features.

Features like backlinks, context menu, related posts, page preview are available by default as they are implemented using CSS and JS. So, you don't have to do anything other than write as you would normally to make use of those features.

#### Note:
When you typeout square brackets, it can be frustrating to type out the entire file title everytime. At least it was for me, so I created a small VSCode plugin, the editor in which I write my essays to autocomplete the titles as soon as I type double squarebrackets. It has been pretty handy for me, if you are interested in using VSCode or already use it, you can find it here: [[Notecomplete::https://github.com/raghuveerdotnet/scratchpad/tree/master/note-complete]]. It is pretty simple to use, all you have to do is just download the note-complete folder and copy it to .vscode directory in your OS to start using it. :)

For setting up the theme on your website checkout [[How to setup Simply Jekyll]]