# 05-Images and Graphics
## Images
> -there are four attributes to include on every image element. 1-The source attribute, shortened to SRC. 2-The alt attribute, ALT. And 3-the width and 4-height attributes.
>```html
><img src="image.jpg" alt="black dog" width="400" height="300">
>```
>-The source attribute is what tells the browser which image file to load.  
-ALT attribute acts as a substitute for the image whenever the image can't be seen.  
-when leave the alt attribute blank, It'll be skipped over and nothing will be spoken aloud.  If we leave off the alt attribute instead, the image file name will get read aloud.  
-width and height attribute let the browser know how big the image is in pixels.  
-the order of attributes in an HTML element never matters, we can put them in whatever order we want.  
-if leave off the height and width attributes, browser has to get the size information out of the file after the image has fully downloaded. This in turn causes jumping around texts as images load and moving everything as we're trying to read.  
-*based on my test and tries*, when working with `<img>` element, following conditions can be occured  
>condition|result
>-|-
>Leave off both height and weight attributes|Image is loaded in its original actual size
>Keep both height and width attributes blank|Image is loaded in its original actual size
>one of size attributes are filled|image size will be changed proportionally
>Both size attributes are filled|image is loaded in its predefined layout
happen to be-is

substitute-to use something or someone instead of another thing or person

shiny-bright because it reflects light

pensive-thinking in a quiet way, often with a serious expression on your face

overly-too; very

wordy-containing too many words

poetic-relating to poets or poems

day care-care provided during the day for young children, esp. in order to allow their parents to work.

split second-a very short moment of time

Head start-an advantage that a person or company has compared to other people or companies

leave off-fail to include someone or something on a list
## Image formats
> -each image format uses a different technique for compressing the image to have the highest quality possible with the smallest file size possible.  
-There are 4 main file formats commonly used on the web today which each is good at compressing certain types of images.  
-gif pros and cons:  
> - One of the oldest image formats  
> - good at compressing illustrations with large areas of a single color  
> - Limited color space of 256 colors which bad choice for photographs  
> - Can be transparent with jagged edges  
> - Can have multiple frames and make animated gif  
>
>-svg pros and cons:
> - Great for logos , icons and other kinds of illustrations
> - SVGs are made of vector and math, ready to quite large or very small without ever losing any quality
>
> Notice: SVG stands for Scalable Vector Graphic, and it's a programming language for graphics.  
-jpg pros and cons:  
> - Great format for compressing photographs
> - Most digital cameras save photos that you shoot as JPG files
> - can be compressed to much smaller sizes, by simplifying the color information in the file. You can pick a balance between the quality and the file size.
>
> -png pros and cons:
> - newer format for the web than GIFs or JPGs
> - sometimes does a better job than a GIF or JPG at compressing the kind of images that the GIF or JPG format likes, but not always.

in quest of-try to find or obtain it

quest-a long search for something that is difficult to find

photograph-to take a picture using a camera

retro-having the appearance of something that existed in the past

tend-to be likely to happen or to have a particular characteristic or effect

jagged-rough and with sharp points

either way-whichever of two given alternatives is the case

keep an eye out for something-to watch carefully for something
## Responsive images
>-Although CSS can show image on big screens or shrink it way down on phones but the following issues occure.  
>-|Pros|Cons
>-|-|-
>high resolution images|great for big screens with high network speed|1- takes a lot of times to download on a slow network connection<br>2-unneeded high resolution data for small and low pixel density screen
>compressed images with low resolution|great for small screens with poor network speed|1-maybe web designs are limited to keeping every images phisically very small<br>2-low quality photo blown up really big on big screens
>
>-More and more screen these days however, are not 1X screens. There are a bunch of retina and high DPI screens out there with a pixel density, is [2X, 3X, 4X](https://devhints.io/resolutions) where more data can be displayed by the screen.  
-The simplest way to support these different screens is to create multiple copies of our image in different resolutions and then tell the browser that those copies are available. The browser will take look at the screen density, the network connection, the users settings and decide which image to use. [Example code snippet](https://codepen.io/imahdio/pen/oNMEBbg)  
-practically, put 1X version of the image at source attribute of `<img>` element. in case of using CSS to adjust image to screen size, the aspect ratio take effects instead of the pixel numbers in width and hieght. inside of `srcset` (source set) attribute we'll list the images with screen density, like 2X, 3X, 4X. the browser will swap out one version of this image for another based on what it thinks is best.
>```html
><img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-480.jpg" 
>     alt="shiny black dog looking pensive" 
>     width="480" height="360"
>     
>     srcset="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-960.jpg 2x, 
>	   	  	https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-1440.jpg 3x, 
>		 	https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-1920.jpg 4x"
>>
>```

shrink down to size-*based on my study friend opinion*, scaling it down, making it smaller to fit the screen size

shrink-become or make smaller in size or amount

cut something down to size-Reduce the size or power of something

glorious-very beautiful or excellent

blow up-a photograph, document, or picture that has been made bigger

coordinate with sb/sth-to work together with another person or organization in order to achieve something

take something into account-consider something along with other factors before reaching a decision

Retina Display-It's a term coined by Apple which means the pixel density on a screen is so high.

coin-to invent a new word or expression, or to use one in a particular way for the first time.

<a name="xfactor"></a> @1x, @2x, @3x- It's refering to [pixel density that makes actual resolution](https://devhints.io/resolutions), not screen size. [More info about PPI calculation](https://www.calculatorsoup.com/calculators/technology/ppi-calculator.php)

swap out-to exchange

## Resposive width
>-*based on my point of view, this lesson has many wrong concepts which incompatible with my test and tries, that's why I try to gather my own assumption based the instructor clues.*  
>-*firefox makes interactive experiment of this lesson exercise*  
>-`srcset` attribute gives you two options for communicating to the browser that there are a set of images available to use either by
>1. the pixel density of the screen or
>2. the width of the viewport
>
>-There are 2 ways to let the browser choose an image from `srcset` attribute based maximum viewport width.  
>1. The `srcset` attribute gives us a way to specify for the browser each image can be shown till which maximum viewport's width. The marks like 480w, 960w means maximum 480 pixels or 960 pixels wide. for example, the following code snippet shows dog-480.jpg up to 960px viewport's width but for wider size till 1440px dog-960.jpg will be loaded and so on.
>```html
><img class="half-width"
>   src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-480.jpg" 
>   srcset="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-480.jpg  960w, 
>           https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-960.jpg  1440w, 
>           https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-1920.jpg 1920w" 
>   alt="shiny black dog looking pensive" 
>   width="480" height="360"
>>
>```
>2. The `sizes` attribute gives us another way to modify already specified maximum width in `srcset` attribute to another breakpoints. for example, the output of following codesnippet is the same as prior one. [compare and Interact with them in here](https://codepen.io/ma400/pen/VwMbOXJ)
>```html
><img class="half-width"
>   src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-480.jpg" 
>   srcset="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-480.jpg  480w,
>           https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-960.jpg  960w,
>	   	  https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-1440.jpg 1440w,
>		  https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/dog-1920.jpg 1920w"
>   sizes="(max-width: 960px) 480px,
>          (max-width: 1440px) 960px,
>          1920px"
>   alt="shiny black dog looking pensive" 
>   width="480" height="360"
>>
>```

viewport-the area in browser windows being currently viewed for example on most mobile devices and when the browser is in fullscreen mode, the viewport is the entire screen.

parse-To parse is to break up a sentence or group of words into separate components; in computer science, is where a string of commands – usually a program – is separated into more easily processed components before transform into machine language. [for more info, check there](https://www.techopedia.com/definition/3853/parse)
## Responsive pictures
>-*like the privious lesson and based on my point of view , this lesson has many wrong concepts which not compatible with my test and tries , that's why I try to gather my own assumption based the instructor clues.*  
>-*firefox makes interactive experiment of this lesson exercise.*  
-this is 3th way to let the browser choose an image from `srcset` attribute based maximum viewport width using `picture` and `source` elements , `media` (which handle the media queries) and `srcset` attributes. in this scenario , When the viewport is a minimum of 600 pixels wide or bigger, the landscape versions of this photo loads and When the viewport is smaller than 600 pixels, the cropped versions loads.  
-check and compare all 3 ways to swap out between different images with various sizes based different browser viewport on [myown modified code snippet in here](https://codepen.io/ma400/pen/bGoRdQg?editors=1100).  
-[here is the original code snippet](https://codepen.io/jensimmons/pen/wvwXLQa?editors=1100) of this lesson which only demonstrate the 3th method.

swap out-to exchange

fantastic-extremely good
## Figure and figcaption
> -`<figure>` element mark up a photo in a document, and a `<figcaption>` element define a caption for the photo. it provides the browser with more semantic contents and let the AI search engines know that these 2 pieces of content have a relationship to each other.
>```html
><figure>
><img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/maggie2.png"
>       width="960" height="720" alt="shiny black dog in the sun">
><figcaption>Maggie the dog enjoys resting in a field, after a long day of chasing squirrels.</figcaption>
></figure>
>```

dug-past and past participle of dig

rather-more exactly

figure-a picture or drawing, often numbered, in a book or document

chase-the act of going after someone or something very quickly in order to catch him, her, or it

squirrel-a small animal covered in fur with a long tail. Squirrels climb trees and feed on nuts and seeds.
## Chapter Quiz
>-SVG or Scalable Vector Graphics can scale to massive sizes without pixelation and still look neat, like they were built for it.
>-The figure element includes or encapsulates the caption element and other graphical elements.
>```html
><figure>
><img src="https://figuresource.com/40289/alfonso.jpg" 
>  width="720" height="354" alt="The Gracious Host" >
><figcaption> Alfonso serving pancakes </figcaption>
></figure>
>```
>-in following code snippet , the largest image is sunsetC.jpg which loads the slowest.  
>```html
><img src="https://storage.net/40785/sunsetA.jpg" 
>      alt="Beach at sunset" width = "512" height="128"
>      srcset="https://storage.net/40785/sunsetB.jpg 1.5x,
>              https://storage.net/40785/sunsetC.jpg 3x,
>              https://storage.net/40785/sunsetD.jpg 2x"
>>
>```
>-You can generate captions from CSS, but you would have to expand your stylesheet every time you added an image. The `<figure>` element keeps your caption with the image and connects them semantically.
-The srcset attribute lets the browser choose from options that fit the specific situation, minimizing bandwidth consumption while producing attractive results.
-Provide pixel measurements (w) instead of 1x, 2x, etc explicitly changes srcset's behavior from a resolution-based srcset to a width-based srcset.  
-in every image element there are 4 attributes including src, alt, height, width. src is short for source, and links to the file. Alt provides an alternative text experience of the image. Height and width let the browser know how much space the image needs before the file is fetched, improving performance.
-we spend effort optimizing image sources and corresponding display attributes to have the best compromise between image quality and download speed  
-we include the height and width specifications for all images to make the page layout more efficient , therefore the size of an image can be learned before download is complete.  
-SVG is best suited to handle complex drawings and logos.

compact-consisting of parts that are positioned together closely or in a tidy way, using very little space

gracious-behaving in a pleasant, polite, calm way

compromise-a situation in which the people or groups involved in an argument reduce their demands in order to reach an agreement.

utilize-to use something in an effective way

