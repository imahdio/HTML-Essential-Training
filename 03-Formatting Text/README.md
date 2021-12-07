## The syntax of HTML elements
> -HTML tags or HTML markups starting out with a less-than symbol, followed by the correct letter, or word, or abbreviated word, and finishing with a greater-than symbol.  
-to markup a paragraph properly, we use an opening tag at the beginning of the paragraph , and then a closing tag at the end. These opening and closing tags travel the world together, in pairs.  
![](https://user-images.githubusercontent.com/64577273/144942422-e53ca8bf-d64c-468d-8583-30d2a3da5d1b.jpg)  
-The whole thing is called an element.  
![](https://user-images.githubusercontent.com/64577273/144942427-1cb11ee5-02ff-4001-95c8-32a1c0e1d94f.jpg)  
-*based on my research and [this link](https://teamtreehouse.com/community/i-do-not-understand-the-difference-between-a-child-and-a-sibling)*  A child relationship is when one element (the child) is inside another element (the parent). A sibling relationship is between two elements that are both inside the same parent element.  
-Although not every element has a closing tag , But a lot of the HTML elements do have both an opening and a closing tag. Like the following:
> ```html
> <p>This is a paragraph.</p>
> <h1>This is a headline.</h1>
> <article>This is an article.</article>
> ```
> -The HTML markup provides computers a way to understand more about what the content, or the interface, means to humans.
-an entire HTML document is a whole bunch of HTML elements all nested inside of each other.  
-The browser pays attention to the structure of how HTML elements are nested and builds a Document Object Model (DOM) tree from the data structure.  
-DOM is the hierarchy and structure of HTML elements , often used for targeting elements in CSS and JavaScript.  
-The browser uses the DOM tree to create an accessibility tree which affects the experience of users on your website, especially ones with various disabilities.

tricky-If you describe a task or problem as tricky, you mean that it is difficult to do or deal with.


nest-to fit one object inside another


convey-to express a thought, feeling, or idea so that it is understood by other people


for effect-said or done to get a particular reaction from someone
## Paragraphs
> -practice online in here:  https://codepen.io/jensimmons/pen/bGbooGB  
-codepen.io is a social development environment for front-end designers and developers and lets anyone make a demo or an experiment by typing HTML, CSS, and JavaScript into related panes.  
-In this exercise we have got HTML describing these text content for the browser to know these are paragraphs of text.

Surf around-to spend time visiting a lot of websites

experiment-to test or to try a new way of doing something

pane-A rectangular area within an on-screen window that contains information for the user

Mess around-behave in a silly or playful way

Blob-based on my assumptions one long string of text
## Headlines
> -Web Pages often have a lot of titles, headlines and subheadlines.  
-in long passage of text , headlines break up the page content to make it easier for people to understand the structure of what's on the page.  
-On Landing pages, those headlines are the content. Titles of things people can click and go on to read more.  
-There are six HTML elements for marking up headlines including h1,h2,h3,h4,h5 & h6.  
![](https://user-images.githubusercontent.com/64577273/144942428-acc57699-9300-4901-a963-4be0a306a6a8.jpg)  
-each headline has different visual effects (ranging from H1 which is biggest to smallest H6) as well as non-visual effects for browsers to understand and communicate about the page.  
-h1 is the main title and h2 is the subtitle for this content.  
![](https://user-images.githubusercontent.com/64577273/144942430-1580e25c-e857-40a5-897b-6120821c1c95.jpg)  
-Html with css can look more modern.  
-NYTIMES uses 3 levels of headlines to markup this section's landing pages.  
https://www.nytimes.com/international/section/arts/dance  
H1 headline represents the title for the whole page.  
H2 headline represents all of the article titles.  
H3 headline represents the little kicker headlines.  
-hierarchical system of headlines define what's most important versus what's less important but it’s possible to semantically display h2 headlines with different font sizes.  
-Making headline levels into an intentional system of hierarchy provides a key interface for navigating a site through sound.  
-defining use cases for each different level of headline make a design system that provides more consistency and semantic success.  
-There is no strict formula about how and when to use each of six levels of headlines. use them to create semantic hierarchy as you wish.

passage-a short piece of writing or music that is part of a larger piece of work

prominent-important

prominence-the state of being important, famous, or noticeable

intentional-planned or intended

strict-strongly limiting someone's freedom to behave as they wish

HTML Semantic Elements-A semantic element clearly describes its meaning to both the browser & the developer. [More example](https://www.w3schools.com/html/html5_semantic_elements.asp)

Kicker-this headline placed on top of the main headline and its purpose is to supplement the main headline which can be used as 1-classic kicker or 2-descriptive kicker

pay off-yield good results; succeed
## Bold and italics
> -There are 4 elements to mark up  text to be italicized or bolded. `<em>` and `<strong>` convey a certain human language meaning while `<i>` and `<b>` are without meaning.  
-`<i>` visual-only italics.  
-`<em>` emphasis italics as well as visual effect which convey meaning.  
-although `<em>` and `<i>` visually mark up text the same but only `<em>` convey human language meaning.  
-`<b>` visual-only bold  
-`<strong>` markup text as bold while conveying meanings like importance , seriousness & urgency.  
-to mark up something on a page typeset , we don't use the strong or B element. We just use CSS to change the weight of the type and apply the style to any element that we want.

typeset-to arrange printed text and images on the page when preparing a book, newspaper, etc. for printing

make a point of doing sth-to take particular care to do something

verbally-using spoken rather than written communication

be tricked-be cheated

get lazy-become lazy

out loud-loudly enough to be heard

implication-a suggestion of something that is made without saying it directly

crave-to have a very strong feeling of wanting something

Thin-not thick

condense-to reduce something, such as a speech or piece of writing, in length

resort- action

throwaway-something disposable or used for a short period of time
## Lists
> -There are three kinds of lists in HTML. Unordered lists, ordered lists, and definition lists.  
-Each list item needs to be wrapped in an `<li>` element which stands for list item.  
-to go along with any 3 kinds of lists , we need to wrap the entire group of items in an element that will mark the beginning and end of the whole list.  
-HTML or browser doesn't care about any additional indentation in front of list items.
> Unordered list `<ul>`|Ordered lists `<ol>`|Definition list `<dl>`
> -|-|-
> `<ul>`<br>`<li>item</li>`<br>`<li>item</li>`<br>`<li>item</li>`<br>`</ul>`|`<ol>`<br>`<li>item</li>`<br>`<li>item</li>`<br>`<li>item</li>`<br>`</ol>`|`<dl>`<br>`<dt>term</dt>`<br>`<dd>description</dd>`<br>`<dd>description</dd>`<br>`<dt>term</dt>`<br>`<dd>description</dd>`<br>`</dl>`
> We use `<ul>` to convey meaning and then use CSS to totally alter how it looks.|Like said before , CSS can be used to restyle lists to look very different from the default styling.|List of definition terms `<dt>` and definition descriptions `<dd>` of each term
> We can leave the content in a list shaped layout or we can lay it out however we want.|We can leave the content in a list shaped layout or we can lay it out however we want.|
> ![](https://user-images.githubusercontent.com/64577273/144982019-4dc43ead-b7b2-4cfc-ae5d-c2a7fb78ed40.jpg)|![](https://user-images.githubusercontent.com/64577273/144982027-ffe8927d-765d-4d5f-b404-488c15641f0b.jpg)|![](https://user-images.githubusercontent.com/64577273/144982036-acd91f81-b890-4293-a161-1c341f17a951.jpg)

> -HTML can mark the end and beginning of the whole list: unordered list , ordered lists and definition lists

teaser-an article, advertisement, short film, etc. that gives a small amount of information about a subject, product, etc. in order to make people interested in seeing or hearing more about it later.

bucket list-wish list , a list of the things that a person would like to do or achieve before they die

indentation-the blank space produced by indenting

ingredient-any of the foods or substances that are combined to make a particular dish

go together-to look good together

recipe-a set of instructions telling you how to prepare and cook food, including a list of what food is needed for this

lay out something -to arrange in a pattern or design; to plan something by showing how its parts fit together

Incredibly- extremely




