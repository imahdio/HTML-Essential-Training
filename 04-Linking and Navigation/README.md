# 04-Linking and Navigation
## Links
> -to make a link we use the A element which stands for anchor element. On the opening tag we need the href attribute which stands for hypertext attribute and point to where we want the link to go. Between the opening and closing A tags, put whatever you want to be clickable.
>```html
><a href="page.html">Link</a>  //link to relative URL
><a href="https://example.com">This is a link.</a>  //link to absolute URL
>```
>-By default, the A element is an inline element. It easily goes in the midst of the flow of some text. [Example codes](https://codepen.io/jensimmons/pres/wvwjERm?editors=1000)  
-absolute urls point to specific absolute places on the web whether home page or any content deeper in. we must include the HTTP or the HTTPS in an absolute URL while including the trailing slash doesn't matter.  
-HTTP stands for Hypertext Transport Protocol.  
-HTTPS stand for Hypertext Transport Protocol Secure.

take something for granted-to never think about something because you believe it will always be available or stay exactly the same

Teaser card- kind of visiting card Where we can put logo,text and link

obsess-If something or someone obsesses you, or if you obsess about something or someone, you think about it, him, or her all the time

obsession-something or someone that you think about all the time

hypertext-text displayed on a computer display with hyperlinks to other text that the reader can immediately access.

hyperlink-a link from a hypertext document to another location, activated by clicking on a highlighted word or image.

hypermedia-an extension to hypertext providing multimedia facilities, such as those handling sound and video.

groundbreaking- innovative; pioneering; showing a new way of doing or thinking about things

End up-to reach or come to a place, condition, or situation that was not planned or expected

obsession-something or someone that you think about all the time

transform-to change completely the appearance or character of something or someone

profound- very great or intense

nerdy-not attractive and awkward or socially embarrassing

throwback-a person or thing that is similar to an earlier type

midst-in the middle of

trailing slash-It’s a forward slash (“/”) placed at the end of a URL such as domain.com/ or domain.com/page/

Get away-escape
## URL paths
> -relative URLs point to local copies of files. It can link to something that’s on the same site in the same domain name as the page that has the link.  
-relative URL isn't just useful for the A element, but to specify a path to a file.  
-To create a relative URL we leave off the domain name, but we include the initial slash at the very beginning. Here are 2 relative URLs for the following image  
/images/logo.gif  
../images/logo.gif  
The first version creates a URL that's relative to the root level. The second version creates a URL that's relative to the file where the URL is typed out.  
![](https://user-images.githubusercontent.com/64577273/145082908-1c0e97e6-786e-41c6-ae56-a7ff47046b10.jpg)  
-The dot dot slash in the second version of the above relative URL means go up a level. This whole path means go from where we are now, up one level, find the folder named images, and then look inside there for the file logo.gif  
-The URL http://www.awesomedogs.com/people , points to the people folder.  
-Anytime the browser is told to go to a URL that is a folder, it automatically looks for an index.html file and loads it. This trick only works for HTML files and makes our URLs pretty or clean. Instead of creating a file named people.html , we can create a folder called people, and inside that folder we put a file named index.html  
-URLs don't matter whether you include the trailing slash or not which means these three URLs go to exactly the same place.  
![](https://user-images.githubusercontent.com/64577273/145082994-27eaf198-59d2-42e5-b50e-aff13cc71bc5.jpg)  
-Using relative URLs can be super helpful on a project that moves from server to server while it's being worked on.

eventually-in the end, especially after a long time or a lot of effort, problems, etc.

leave out something/someone-to fail to include something or someone; omit

relative- considered in relation or in proportion to something else

from scratch-from the very beginning

elegant-graceful and attractive in appearance or behaviour

craft- to make objects, especially in a skilled way

type out- the act of typing

craft-to make objects, especially in a skilled way
## Navigation
> -the nav element is for marking up navigation. It tells the browser which sets of links are part of the site navigation. We don't use it all the time, just for major blocks of navigational links.  
-to convey the purpose of the main menu for *screen readers and other assistive devices* , we can add `roll="navigation"` to the nav element. It’s an ARIA roll that conveys extra kind of importance for marking the main navigation of the page. It adds the extra kind of importance that's conveyed to other people visually through graphic design.  
-aria-label="true" provides a label that can be read aloud by the screen reader.  
-this [Example code](https://codepen.io/jensimmons/pen/rNBvqKL?editors=1000) make main menu using unordered list and CSS as first example for using set of links  
![](https://user-images.githubusercontent.com/64577273/145083000-bf70f17e-6bb5-4c8b-8162-063028ddaf67.jpg)  
-this [Example code](https://codepen.io/jensimmons/pen/dybKOxm?editors=1000) makes breadcrumb trail navigation menu using ordered list and CSS as second example for using set of links.  
![](https://user-images.githubusercontent.com/64577273/145083002-60df0ac3-79da-4650-b0a3-b876ef0614bb.jpg)  
-*based on my assumption* , there must be such the following table
*I reached some unresolved conflicts if the following table is true!!*  
![](https://user-images.githubusercontent.com/64577273/145083004-c2e9022f-c081-49c9-b65f-4658ab3039b3.jpg)  
-this [Example code](https://codepen.io/jensimmons/pen/vYBrgYz?editors=1000) makes footer using footer element and CSS while It’s not really part of a navigation as third example for using set of links  
![](https://user-images.githubusercontent.com/64577273/145083009-ad428b43-988d-4669-8cef-d9b24afc426e.jpg)

major- important, serious, or significant

breadcrumb trail- this navigation path allows users to keep track and maintain awareness of their locations within programs, documents, or websites

The only for sure is that it depends- it depends on users to choose a way
## Chapter Quiz
> -CSS can change the way that a list and other objects are presented.  
-There’s no single correct way to mark up navigation, but often developers use  `<nav>`, `<ul>`, `<li>`, `<a>`  
-`<a href="https://example.com">text to click</a>` is the format for a link.  
-when a website might be moved from a staging server to a production server we need to use a relative URL instead of an absolute URL.  
-`"/people"` looks for index.html in the people directory.



