# 03-Understanding the power of HTML
## Debugging HTML
> -to inspect HTML in a browser developer tools either right-click on a web page and go to inspect element, or instead we can go to tools> web developer> inspector. Here is sample codeBlock: [link1:Editor View](https://codepen.io/jensimmons/pen/xxKjYRR?editors=1100) / [link2:Debug mode](https://cdpn.io/jensimmons/debug/xxKjYRR)  
-Developer tools acts like cockpit of controles.  
-There are 3 panes in inspector tab. On the left is the HTML, the middle is for CSS and the right pane has several more options. The DOM or Document Object Model that browser has created is shown in left pane.  
![image](https://user-images.githubusercontent.com/64577273/146134536-11e55464-5ab8-4df8-adeb-fa1af15f0452.png)  
-Browser read the html page and revise any mistakes that I might have had and create the Document Object Model or DOM tree.  
-we can use developer tools to inspect any website on the internet to get ideas when we’re not sure what markup to use on a similar project.  
-HTML inspector can be used to debug mistakes after comparison with its DOM version. [For example in this link](https://codepen.io/jensimmons/pen/aboGBML?editors=1000) a blank item throws off the counting and we get 5 items instead of 4 ones.

inspect-to look at something carefully in order to check its quality or condition

cockpit-It’s the area, usually near the front of an aircraft or spacecraft, from which a pilot controls the aircraft.

revise-to change an amount or value in order to make it more accurate

turn sth-to change in position usually by moving through an arc of a circle

peek-look quickly or furtively (secretively)

peek under the hood-To examine the internal workings of sth

throw off something/someone-to cause an amount to be wrong or a person to be confused

What's going on? -What has happened or is currently happening?

sort something out- to understand or find (something, such as a reason or a solution) by thinking

furtively- secretively

## HTML attributes
> -some HTML attributes only work on certain elements like datetime attributes which only use on time elements. Other attributes work on several elements but not all of them.  
-global Attributes are attributes in HTML that will work on any element.  
-class is a global attribute that allows us to target (point) all elements of a html document **with that class in our CSS or JavaScript**.
> ```html
> <p class="intro">content</p>  //true
> <p class="class1 class2">content</p>  //true
> ```
> -id is a global attribute that is similar to class but we’re only allowed to use one specific id in each HTML element. *(based on my own test and tries and study friend’s opinion, I revised this hint due to wrong believes in main quotation)*
> ```html
> <p class="class1 class2" id="id1">content</p>  //true
> <p class="class1 class2" id="id1 id2">content</p>  //wrong , cannot use several id like class in one element
> ```
> -although we can use either class or id for targeting css but class is best for css more than id.  
-ids are particularly helpful for addressing particular elements with JavaScript or, with a targeted link. That’s why It’s a good convention to use just one element with any particular ID name in an entire HTML page **when interacting with javascript or links**. [For example in this link](https://codepen.io/imahdio/pen/eYjyjqp) , there is a table of contents with links that jump to the elements that have the matching ID.  
-`contenteditable` is a global attribute that lets a visitor to a page edit the content of that page. Notice that it doesn’t change the content in the HTML and if you refresh the webpage , it goes back to the original. [Code link](https://codepen.io/imahdio/pen/oNMpPjG)  
-`lang` is a global attribute that tells the browser what language the content is in.  
-`dir` (stand for direction) is a global attribute that gives us a way to explicitly tell the browser in which **direction** the text flows.  
![](https://user-images.githubusercontent.com/64577273/145069325-c8972710-d735-4a03-9956-cbba75a4eace.jpg)  
-Class , ID , Lang and Dir are 4 most important global attributes. List of global attributes can be found in MDM web docs.

You can use an ID for targeting CSS, but it's much more specific and that can be a problem- that's mean class is best for css more than id

particularly-especially, or more than usual

Assistive devices -assistive equipment is designed for people who have physical difficulties and need help with using things like computers

hook into sth- to connect to sth

mumbling-speaking or spoken in a quiet and indistinct way
## ARIA roles
> -ARIA roles are HTML attributes that make layer of informaion to  tells [screen readers](https://chrome.google.com/webstore/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn?hl=en) and other assisitve devices semantics of the contents about not ideally proper elements. in this example if we don't use ARIA roles, screen readers say words separately. [Editor View](https://codepen.io/imahdio/pen/poZpOrj) | [debug mode](https://cdpn.io/jensimmons/debug/wvwjxJa)  
> -Browser uses HTML to build DOM trees. And then takes the DOM tree to build the accessibility tree. The accessibility tree is what [screen readers](https://chrome.google.com/webstore/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn?hl=en) and assistive devices use to provide an experience of the website through a screen reader which make your website accessible for every one.  
> -[In following example](https://codepen.io/ma400/pen/VwMpYyq) , `aria-label` attribute determine the proper sentence that screen reader will read and `aria-hidden="true"` removes inappropriate element with all of its children from the accessibility tree.  
>```html
><h1 aria-label="hello world">
>    <div class="grid" aria-hidden="true">
>        <span>h</span>
>        <span>e</span>
>         ...
>```

compromise-an agreement in an argument in which the people involved reduce their demands or change their opinion in order to agree

it's gone-it has disappeared, it has been lost

deserve-do something or have or show qualities worthy of
## Formatting HTML
> -HTML doesn’t care about spaces beyond the presence of single space except if we use a `<pre>` , `<code>`(which commenly be used inside `<pre>`) or  `<textarea>` or use CSS to change how the white space is handled. [check it in here](https://codepen.io/jensimmons/pen/MWgGVqr?editors=1000)  
-`<!-- custom comment -->` add comments to code for documentation and easier understanding. [Example link](https://codepen.io/jensimmons/pen/ExYLRmg?editors=1000)  
-code editores gray out commented code or remarks. It prevents us from being confused about why something is not working.  
-HTML doesn't mind capitalizing elements with uppercase letters or keeping them in lower case.  
-Because in ancient times scientists were obsessed with counting every single bit and bite due to very low capacity of RAM & HDD , the length of `<i>` and `<p>` elements are very short while newer elements use whole words like `<video>` or `<article>` that’s why “the length of an element, it's a bit of a clue as to how long an element has been around.”  
-kinds of elements with different requirements to use opening & closing tags
>description|element
>-|-
> Elements with both opening and closing tags|![](https://user-images.githubusercontent.com/64577273/145069334-a1c11e46-aab1-4000-a3f0-01cf39437859.jpg)
> Elements that don't have anything between opening and closing tags by default|![](https://user-images.githubusercontent.com/64577273/145069337-bb709db3-4798-446b-861c-6718292f06dd.jpg)
> Some older elements not have closing tag|![](https://user-images.githubusercontent.com/64577273/145069341-acc492fa-fdf1-4567-9d40-4d383090ad97.jpg)

carriage return-a character that tells a computer to move the cursor to the beginning of the line; The `<br>` HTML element produces a line break in text

ancient-of or from a very long time ago

evolve-develop gradually

1980s-the decade from 1980 to 1989

scientist- an expert who studies or works in one of the sciences

obsess-If something or someone obsesses you, or if you obsess about something or someone, you think about it, him, or her all the time

clue-a sign or some information that helps you to find the answer to a problem, question, or mystery

out there-in a place that could be anywhere except here
## Weird characters
> -Html entities are formatted like this. Ampersand, some kind of short code, and a semicolon. We type them into an html file and they get converted into the characters that we want.  
-Html entities are helpful for  
>1. write any html elements like the `<` or `>` or `ampersand(&)` as text phrase and prevent browser to treat with it like html codes
>
> Html entity | character
> -|-
>`&lt;` | `<`
>`&gt;` | `>`
>`&amp;` | `&`
>
> Notice: if we directly write a `<` or `>` or `&` symbols with spaces around it, it will show up as common content without any problem.  
Notice: If you are writing html elements inside a content management system like WordPress or using a tool like markdown, there's a chance that the layer between your text editor and the pure html will handle these characters for you just fine by adding correspond HTML entities.  
>
>2. Type special characters that not existing on keyboard
>
> Html entity|character
> -|-
> `&copy;`|`© (Copyright symbol)`
> `&trade;`|`™ (Trademark symbol)`
> `&star;`|`☆`
>
>Notice: we can copy special characters instead of typing entities.  
Notice: W3C keeps a reference chart of all the character entities.
>
>3. Non breaking space (`&nbsp;`) prevents browsers from breaking line on that space. [Example code](https://codepen.io/imahdio/pen/xxJpBNE)  
Although browsers ignore everything beyond the first regular space, the non-breaking space can also force the browser to put more than one space between words. [Example code](https://codepen.io/imahdio/pen/oNMpVRW)  
>
>Notice: we can put two spaces between each sentence, if one of those spaces is a non breaking space.

show up-be conspicuous or clearly visible

Markdown tools-It’s simple and user-friendly text-to-HTML conversion tools for web content writers. Developers and content creators can use them to format lists, headers, and many other content features.

correspond-to match or be similar or equal

wrap-to cover or surround something with any materials

word wrap-line breaking, this feature breaks lines **between** words rather than **within** words.
## Chapter Quiz
> -user can gain access to the debugging features of a browser by accessing developer tools  
-The dir attribute is global. It stands for “direction” and can be used on any element to specify the direction of inline flow for that content.  
-The datetime attribute is only used on the time element, as a way to create a machine-readable date.  
-ARIA is used to clarify to the accessibility tree what is happening with a particular element, set of elements, or interface. If something is broken, ARIA can be a way to fix it.  
-in case of accessibility issues we have to use and understand ARIA attributes.  
-the output from the following code appear like
>```html
><h1> This is a test. </h1>
><p> If this were an actual emergency, 
><!--  Should there be an actual emergency? -->
>  there would be panic.
></p>
>```
>![](https://user-images.githubusercontent.com/64577273/145069343-dfa4f585-55b8-4fcf-81a2-6baad55b273c.jpg)  
Notice: *based on my study friend opinion* , in spoken language we can use were instead of was in front of things that are not physical. in above sentence an emergency is not something you can touch therefore were is used instead of was.  
>Notice:  The `<!--` introduces a comment that is not interpreted. The `-->` closes that comment.  
-use `Hocus&nbsp;Pocus` guarantee that the words "Hocus Pocus" are not split by a line break after "Hocus". In other words , The non-breaking space character entity (`&nbsp;`) ensures that "Hocus Pocus" will always display on the same line.  
-we might use developer tools in following conditions
>1. Something seems wacky and you aren't sure what is causing it.
>2. when you need to figure out how to apply CSS or JavaScript to a certain part of the markup.
>3. when you want to see the DOM the browser has created from your HTML.
>
>-this code `< test >` produce this output `<test>`, Although there are other ways to produce the same output.  
-we can add `&nbsp;` to any characters to appear as simple text instead of being parsed as code.  
-the characters < and > are hard to present in HTML, as the code thinks they are the beginning of a tag. So instead we use the character entity `&lt;` for < and the character entity `&gt;` for >  
-An id attribute refers to one specific part of a document.

panic-to suddenly feel so worried or frightened that you cannot think or behave reasonably, or to cause someone to feel this.

wacky-weird or nutty or silly

nuts-mad