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
> ![](https://user-images.githubusercontent.com/64577273/145017232-83998ced-59a5-4b96-a23b-67fa639f737a.jpg)|![](https://user-images.githubusercontent.com/64577273/145017239-216db8e1-2086-4bc5-91b7-6d6736005c70.jpg)|![](https://user-images.githubusercontent.com/64577273/145017242-bbed4537-9243-4c4d-9a33-5759a4acd116.jpg)
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
## Quotes
> -`<cite>` and `<blockquote>` are being used for their HTML semantic value. They convey meaning to other computers and convenient places to use target styling through CSS.
-in following snippet , we use `<cite>` element to credit jeremy as the person who said the quote and wrap the whole thing in a `<blockquote>` element to distinguish it from surrounding text.  
![](https://user-images.githubusercontent.com/64577273/145017243-3076e0f4-2062-48ba-8d22-9e6e9b933c2d.jpg)  
-*based on chapter Quiz lesson* The `<cite>` element identifies sources.  
-we can put any element inside the blockquote like list or headline while nested inside each other.  
-`<q>` stands for quote and lets the browser provide the quote marks for us instead of typing the quotes manually.   Its typography shape depends on the language and types of conventions of a particular region can be straight quote marks or curly quote marks.  
-inline elements wrap around phrases of content that are inline with some other contents like `<q>` , `<strong>` , `<b>` , `<i>` and `<em>` and etc. all other elements are block-level elements like `<blockquote>` , `<p>` , `<ul>`.   They are blocks that can be followed by another block.
![](https://user-images.githubusercontent.com/64577273/145017249-84c5c983-8723-4392-bd5b-b38ac95b45c5.jpg)  
-when you use CSS you can switch the layout behavior from block to inline or from inline to block.  
-*CONFLICT! Based on my tests and tries* , we can use `<ul>` blockquote element nested `<p>` blockquote element which is against the definition of blockquote elements.

passage-a short piece of writing or music that is part of a larger piece of work

quote-to repeat words that someone else has said or written

cite-refer to (a passage, book, or author) as evidence for or justification of an argument or statement, especially in a scholarly work

`<cite>` Tag -defines a person's name or the title of a creative work.

`<blockquote>` Tag -specifies a section that is quoted from another source.

stand out- to be very noticeable

Curly quote and straight quotes-check these examples

intuit-to know or understand something because of a feeling that you have rather than because of facts or what someone has told you.

nerdy-

Typography- the style and appearance of printed matter
## Dates and times
> -With HTML time element and its datetime attribute , we communicate time semantically(let’s convery meaning for other computers).  
-Although We can use any human understandable format for the phrase of text that's between the time tags, the whole point of time element is HTML attribute which only uses a standardized machine-readable format to convey other computers exactly when this date or time is.  
-Here are the machine readable phrases in the datetime attribute:
> parameter|machine-readable format|example
> -|-|-
> Date|YYYY-MM-DD|![](https://user-images.githubusercontent.com/64577273/145017256-bd06a6fe-ddf0-4ddc-9d15-3c294f6bb83b.jpg)
> Times|24hour clock format:<br>hh-mm|![](https://user-images.githubusercontent.com/64577273/145017258-b23f20e4-108a-4ff0-9f68-57c1f00bed54.jpg)
> "|include seconds & fractions of a second or not:<br>hh-mm-ss.ddd|![](https://user-images.githubusercontent.com/64577273/145017260-f304871f-03a3-453a-a53c-778da0ec08a6.jpg)
> "|include time zone from greenwich time:<br>hh-mm-ss.ddd+-hh:mm|![](https://user-images.githubusercontent.com/64577273/145017265-2d1a6784-c33f-46e6-9e3f-facd2e80c910.jpg)
> Date and Times together|between the date and time either put T or a space|![](https://user-images.githubusercontent.com/64577273/145017268-85bdc83d-aad4-475c-a05e-4978ab58ec06.jpg)

> -Other different format of machine-readable date time in HTML and many other programming languages:  https://lnkd.in/g7eqZhE

Messy-untidy

span-the period of time that something exists or happens
## Code, pre, and br
> -`<code>` element stands out any code phrase from HTML context to look like code  
![](https://user-images.githubusercontent.com/64577273/145020699-41c11361-3e96-4cf4-9c94-52537de9a09f.jpg)  
-we can use the following html entities to show on the page instead of being executed.  
> Greater than| > |`&gt;`
> -|-|-
> Less than| < | `&lt;`

> -`<br>`is simple single HTML tag which adds line break and browser respect it
> ![](https://user-images.githubusercontent.com/64577273/145020704-79e15123-68cd-4ebb-9964-2e59648bf755.jpg)  
> -`<pre>` make the browser pay attention to any indentation and line breaks in html context.
> ![](https://user-images.githubusercontent.com/64577273/145020707-9a47ac23-c8ec-4af1-9fa1-3d945aa1b8e2.jpg)
> -`<pre>` and `<code>` are frequently combined to show a block of code with indentation. In the following example , the whole code is wrapped in `<code>` element to convey meaning of code for browser and other computers and all of that is wrapped in `<pre>` element which maintains the semantic formatting and spacing.
https://codepen.io/jensimmons/pen/gOYvjpa  
> ![](https://user-images.githubusercontent.com/64577273/145020718-e04cf912-2f97-4232-a20b-1eacec79ca59.jpg)

Stand out-to be easily seen or noticed

monospaced font- It’s a font whose letters and characters each occupy the same amount of horizontal space.

character entity- It’s a code used to represent a character that doesn't belong to the document's character set.

HTML entity- It’s a piece of text ("string") that begins with an ampersand ( & ) and ends with a semicolon ( ; )

entity-a thing with distinct and independent existence

Mash up-mix or combine two or more different elements

piles of (something)- a lot of something


  










