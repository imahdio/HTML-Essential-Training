# 07-More Ways to Identify Content
## Supporting languages
>-if our whole page is in the same language, we can set the language on the outermost element that wraps all the other elements. for example  
>* lang="en-US" stands for U.S. English
>* lang="en-GB" stands for British English
>
>-the lang attribute is a universal attribute , meaning you can put it on any element.
-if the majority of a page is written in Mexican Spanish (`lang="es-mx"`) , for instance, but there are several block quotes written in Nahuatl (`lang="nah"`) we could arrange it like this:
![image](https://user-images.githubusercontent.com/64577273/147047810-277c1616-e361-401a-ae2d-41a3dd308888.png)
-Specify the direction our content flows with the `dir` attribute which is a universal attribute that can go on any element like the following examples:
>```html
><html lang="en-gb" dir="ltr">
><html lang="ar" dir="rtl">
>```
>NOTICE: When you mix content, you want to mark each phrase with the change of directions.  
-all of the human language , characters, letters, and symbols are written in a script and in a format for computers to understand.  
-`charset` attribute defines the alphabet or set of characters for the script language.  
-ASCII is an encoding standard limited to 128 characters basically the characters from an English language typewriter.  
-Unicode or UTF-8 is a universal encoding standard for characters encompassing many languages. It supports every language, all scripts, all form of communication, including Braille, sign writing, musical notation, and almost 3000 emoji.
-following code specify the charset for HTML.
>```html
><head>
><meta charset="UTF-8">
></head>
>```

by its very nature-because of the nature of the subject

propagate-to spread opinions, lies, or beliefs among a lot of people

encompass-to include different types of things
## Generic elements: div and span
>-`<div>` and `<span>` are two elements that you can use anytime none of the other elements make sense.  
-Before 2010, before HTML 5 brought us so many of the semantic elements that we need, we used divs for all sorts of use cases.    
-Although it's possible but don't use `<dive>` and `<span>` for everything.   -`<div>` is block level element and `<span>` is an inline element. They both do the same thing Until you point CSS or Javascript at them.  
-in following code snippet , We've got a simple article wrapped in an article element. There's a headline and four paragraphs. to put these paragraphs in a group together so that we can put a background color behind just the paragraphs and not behind anything else , add a `<div>` with a class of box. to change the `lang` attribute for the sentence in the middle of a paragraph let's use the inline element `<span>` to mark the phrase that we want to change. [Link to code example](https://codepen.io/jensimmons/pres/dybjNLQ)  
>```html
><article lang="en">
>  <h1>This is the headline</h1>
>  <div class="box">
>    <p>The first paragraph.</p>
>    <p>Some text in a second paragraph.</p>
>    <p>Third paragraph. <span lang="es" class="bilingual">Esta oración está en español.</span> Some of this text is in another language.</p>
>    <p>Fourth paragraph.</p>
>  </div>
></article>
>```  
>-`<div>` and `<span>` can take all the global attributes of course, class, id, lang and aria roles. Use them when there's not another appropriate element as a last resort.

likly-probably

get away-escape

colleague-one of a group of people who work together

resort-the fact that you have to do something because there is no other way of achieving something
## Chapter Quiz
>-we can mark a quotation as being in a different language from its surrounding text with `<blockquote>` element and a `lang` attribute indicating the language for its contents.  
-The only difference between the usage of `<div>` and `<span>` is that `<div>` is a block level element, and `<span>` is an inline element.  
-There are many reasons for specifying the desired language for HTML content including to ensure the correct dictionaries and pronunciations are used.  
-The `<div>` and `<span>` elements make it easy to create containers or labeled content for styling.