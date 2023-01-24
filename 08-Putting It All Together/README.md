# 08-Putting It All Together
## The HTML page
>-HTML files are key building block of the web.  
-a user goes to a URL, hitting that URL sends a request for an HTML file, a server returns a single HTML file, the browser reads the HTML file and does what it says.  
-Text frequently is stored in a database or multiple static files often pull together the last millisecond, custom for each user. Visual styling is in CSS files, JavaScript is in separate JavaScript files, plus the images, video, audio files, advertisements.  
-When the browser gets html file, it immediately starts reading it from top to bottom and starts to do what it says.  
-Once the HTML file is built, there are several key parts that every web page must have.
>1. First, the file must start with a `<!doctype html>`, This little statement declares which era this HTML file is from. So by including this one, we tell the browser this is a modern web page, cut it with modern best practices.
>2. Then, we wrap everything else on the page with an `<html lang="en-US" dir="ltr">` element to declare which language we're going to use and in which direction the content should flow.
>3. Then inside `<html>` element, you have two major parts where everything goes. The `<head>` and the `<body>`. The `<head>` is for all the metadata, all the stuff about the document that a browser needs to know but will not be displayed on the page.
>4. the `body` element contains the information and content that will be displayed on the page.
![image](https://user-images.githubusercontent.com/64577273/147146582-fac40800-eaab-4e15-b1db-8cca1a198a53.png)

implicit-suggested though not directly expressed

pull together-cooperate in a task or undertaking, to work hard as a group in order to achieve something

mishmash-a confused mixture, a badly organized mixture

headquarter-the management team who work at a headquarters

off to the races-ready to begin something exciting

prescribe-to tell someone what they must have or do, or to **make a rule of something**

era-a period of time known for particular events or developments

declare-to announce something clearly, firmly, publicly, or officially

cut it-to handle , to successfully complete or accomplish a desired or expected result

as such-using the exact meaning of the word or phrase

right up front-before we speak of anything else

prescribe-to tell someone what they must have or do, or to make a rule of something

metadata-a set of data that describes and gives information about other data
## Document head
>-The meta elements only used inside the head and conveys metadata about the page. It's not content that you want the users see. It's information about this website that you want the browser to know.  
-we need the following elements, inside the head of every HTML page:
>* `charset` attribute to define the character set, and set it to utf-8
>* `<title>` element is not a title that gets displayed as content. It's a title for the webpage that's used by the browser. It shows up as the name on a browser tab, or as a bookmark title
>
>code|result
>-|-
>![](https://user-images.githubusercontent.com/64577273/214137110-c771d5ad-8f4a-449f-b827-5dae938001d9.png)|![](https://user-images.githubusercontent.com/64577273/214137449-b04fadd2-a47e-4e6c-b1de-9b6cc5bdedb7.png)
>
>-we might want to have other elements inside the head of the page like:
>* The meta element can be used to define all kinds of settings.
>* * One incredibly common use is to tell the browser the layout has been morphed to fit small screens, that it is a responsive website. [Check here for more details](https://www.w3schools.com/tags/att_meta_name.asp)
>```html
><meta name="viewport" content="width=device-width, initial-scale=1">
>```
>* * We probably also want to add a description of the site. This description will show up in search engine results.
>```html
><meta name="description" content="A description of this site that will show up in search engine results.">
>```
>* * to give a webpage name when it's saved to home screen and to specify tile image and a background color of the website icon either in windows metro interface or on phone devices. [Check here fore more details](https://github.com/imahdio/HTML-Essential-Training/issues/9)
>```html
><meta name="application-name" content="Filament Group">
><meta name="msapplication-TileImage" content="/images/icons/mstile-144×144.png">
><meta name="theme-color" content="#247200">
>```
>* `<link>` element is used to link to a range of other assets that we want to load, like CSS files, fonts, and favicons. The `rel` attribute is used to tell a browser which kind of asset it is. the `href` attribute is used to provide the URL to the asset.
>```html
><link href="main.css" rel="stylesheet">
><link rel="icon" href="favicon.ico">
><link rel="preload" href="myFont.woff2" as="font" type="font/woff2" crossorigin="annonymous">
><link rel="manifest" href="/webappmanifest.json">
>```
>Notice: the browser will load the files in the order in which they're listed. Put things you want to load first at the top. Things that aren't as important or that won't get used right away, they can go further down.  
>* The last commonly used element that goes into an HTML document's head is the script tag. This tells the browser to load a JavaScript file. Actually, a script tag doesn't have to go into the HTML head. Frequently, people put it at the end of an HTML document so the browser loads JavaScript after everything else has loaded. But sometimes it is included in the head.
>```html
><script src="my-javascript-file.js"></script>
>```

incredibly-extremely

morph-to change gradually in appearance or form

shrink down-to become or cause to become smaller in size

tiles image-It's the behavior of a widget to display one or more repetitions of an image
##  Structuring content
>-there are six major elements that make overall structure of document body includes `main`, `header`, `footer`, `article`, `section`, and `aside`. It's the semantic meaning that matters here, not the position on the page
>1. the `main` element wraps around the main content of the page. It's only used once per webpage, and it tells the browser, this is where the main content is.  
>2. the header and footer elements are used to mark places on the page where the content is a header or a footer.  
>**Notice:** don't confuse header with head. Head is part of our HTML document that's never displayed to users where the metadata for the file lives. Header is used to wrap site headers, article headers, headers in the content.
![image](https://user-images.githubusercontent.com/64577273/147284065-2a8c57a5-4edd-4091-abe1-2e9ae07bf3a8.png)  
>3. many webpages end with a footer at the bottom, with lists of links, some copyright information, extra information about the company that would naturally be wrapped in a `footer` element. That kind of information is actually well-suited for a `footer` element because the semantic meaning that matters, not the visual display.  
>4. `article` is wrapped around any instance of an article. It might be a long written article or blog post. It might be a very short snip. A teaser card can be marked up as an article element. A tweet or social media post, that can be an article. The article element just means, this by itself is a unit of content.
>5. `section` is used to wrap around sections of content. If we have a long essay for instance, that's broken up into chunks with sub headlines, we can use the `section` element to mark each segment. It's a flexible element that means, okay, let's just start with another thing. Usually each section has its own headline marking the start of a new segment of content.
>6. `aside` is for marking something that's off to the side. Perhaps in a side bar, or any content that's kind of not the main attraction. It could be an inset panel that goes with a big article giving additional information, but isn't quite part of the flow of the article itself. Or advertisements, they are a side thing perhaps best marked as an aside.  

suit-to be convenient or work well for someone or something

instance-a particular situation, event, or fact, especially an example of something that happens generally

snip-a small piece of anything (especially a piece that has been snipped off)

Off to the side-aside or apart (from a group or main area of something), especially to be out of the way or out of earshot

overall structure-overall form or organization of something

somehow-in some way

stuff-matter, material, articles

essay-a short piece of writing on a particular subject

chunk-a part of something

segment-each of the parts into which something is or may be divided

zone-an area, especially one that is different from the areas around it because it has different characteristics or is used for different purposes

off to the side-the side or not the main attraction

inset-a thing that is put in or inserted
## Examples of putting it all together
>-When I'm not sure what the best way to mark up a page is , I travel around the web, finding similar sites, and I use developer tools to see how other folks have decided to use HTML elements in their content.  
-There's a bit of an art to structuring HTML. We have a lot of creative freedom here.

play off of sth-to use that thing as a starting point for some variation

add up to something-together they form that total , to have a particular result or effect
## Chapter Quiz
>-The `<p>` tag is used almost exclusively in the body.  
-The html element contains the body element, and the `<title>` goes in the head and not the body. Also, `<picture>`, `<p>`, `<table>`, and `<form>` operate a layer below the sectioning.  
-`<aside>`, `<main>`, `<article>`, `<header>`, `<footer>`, `<section>` are the six major sectioning elements that typically go directly in the `<body>` element.  
-`<header>` is most appropriate for the blue bar in the following image which can be used inside `<article>` and `<section>`.  
Notice: The `<title>` element is a document specification; it does not necessarily appear on the page.  
>![image](https://user-images.githubusercontent.com/64577273/147327807-bce8d6d5-3637-480b-a686-119402018fc6.png)  
-The `<header>` element contains the document title , and the `<head>` element usually contains a `<title>` element.  
-`<Header>` contains information that is displayed as part of the `<body>` and the `<head>` element contains a list of files to be included.  
-The head element contains document metadata, and a header element can occur at several locations within the body.  
-the head of an HTML page should contain metadata.  
-`doctype` is a mandatory declaration at the beginning of every web page.  
-The browser parses a single HTML document, which may also include links to other resources, which the browser then downloads and presents.  
-While a browser does start by making a request to a URL, a single HTML document is usually the key payload, not multiple.  
-`<title>` element inside of the `<head>` element identify the page when it's bookmarked. The `<title>` element provides the bookmark information.  
-`<section>` could be a paragraph or a group of paragraphs united by subject or focus.  
-an `<aside>` element is appropriate for footnotes or diversions from the main topic. it's most appropriate to implement the pink box in the above image too.

exclusively-only

diversion-the action of turning something aside from its course