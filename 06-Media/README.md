# 06-Media
## Audio
>-`<audio>` element used to place audio files on a webpage and it can trigger the browser to create an entire audio player interface for us.  
-the both an opening and closing tag gives `<audio>` element more power and flexibility. `src` attribute provides the URL to the file.  
-`controls` attribute trigger the optional controls that are built into the browser includes  a play button, a timeline, a volume control. We could instead make our own custom controls using JavaScript and the HTML media element API too.  
-`loop` attribute start playing from the beginning again.  
-`autoplay` attribute will cause the audio to be played automatically as soon as the page loads, at least in some browsers. Notice most people actually hate it when the audio starts playing automatically when they land on a webpage.  
>```html
><audio controls loop autoplay src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/birds.mp3"></audio>
>```
>-we can use `<source>` element to specify more than one audio file. perhaps you want to use a new file format that's not supported in every browser while providing a fallback for the older browsers. The browser will use the first file that it understands in the list. You can also provide some fallback text that will only be displayed if the audio element is not understood by the browser at all. [original example same like following code snippet](https://codepen.io/jensimmons/pres/BaBVdWp?editors=1000)  
>```html
><audio controls loop autoplay>
>   <source src="birds.ogg"
>           type="audio/ogg; codec=opus">
>   <source src="birds.mp3"
>           type="audio/mpeg">
>   Sorry your browser doesn't support this audio.
></audio>
>```
>-MP3 are supported in most modern browsers today and OGG is another audio file format that had some advantages but it never became very popular. It seems that a new format may come out soon, the cousin to the AV1 video file format.  
-we need to be familiar with `<source>` element for supporting multiple formats since it was important for a while and it's likely to be very useful again sometime in the near future.

fallback-an alternative plan that may be used in an emergency

resilience-the quality of being able to return quickly to a previous good condition after problems

trigger-cause (a device) to function

cousin-a child of one's uncle or aunt

AV1 video file format-AV1 is a new video codec with 30% more efficient than High Efficiency Video Coding or H.265

## Video
>-One way to put video content on a webpage is to use the `<video>` element in HTML.  
-`source` attribute point to a video file.  
-`control` attribute tells the browser to create a video player for us.  
-mp4 video file is compressed using H.264 codec. The H.264 codec currently has the widest support across browsers.  
-any internet video is using a pretty hefty mechanism for smashing all the data into the smallest possible package.  
-There've been many attempts to make the ultimate codec, Real Video, Sorenson, Windows Media, Flash, H.263  
-The H.264 codec is the one that's dominated. it's not open source, it's patented. It's owned by a consortium that charges fees for every device wants to be able to record, compress or play H.264 files. And, they are about to charge way more for H.265  
-this instructor believes like html and public image formats , none of the underlying technology on the web should be patented. To fix this, a lot of effort has gone into creating a truly open, not patented, but still super awesome video codecs like WebM and AV1. Time will tell on how things shake out.  
-`source` element list the multiple file formats. `src` attribute link to the file, and the `type` attribute tell the browser which type of file it is. The browser will play the first file that it understands. [Following Code on codepen.io](https://codepen.io/jensimmons/pres/VwZdzBe)
>```html
><video controls>
>	<source src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/moonwalk.480p.vp9.webm" 
>  			type="video/webm">
>	<source src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/moonwalk.480p.h264.mp4" 
>  			type="video/mp4">
></video>
>```
>-there's nothing in HTML that will allow us to send different sizes of video under different network c that's because we don't want the device to get only one moment to make a choice between standard def and high def. We want it to make that choice over and over again while playing the video.  
-All video apps like youtube are constantly switching from one resolution to another as people watch, using a technique called adaptive bitrate streaming which is really complicated and requires a Data Center of transcoding robots. that's why when you go to put video on a website, it's likely you might not use the video element , instead use embed code from a video hosting service.

revolutionize-to completely change something so that it is much better

transform-to change completely the appearance or character of something or someone

transmit-to broadcast something, or to send out or carry signals or messages using radio, television, etc.

hefty-large in amount or size

smash into-hit object against another with great force , to cause someone or something to collide into someone or something with great, violent force.

ultimate-being or happening at the end of a process; final

dominate-to be more important, powerful, or successful than other people, companies, etc

patent-to get the official legal right to make or sell an invention

consortium-a group of companies, organizations, etc. that have joined together to work on a particular project

underlying technology-*based my study friend opinion* fundamental or basic technology and to get into more details it is refering to html css and javascript

emerge-to appear or become known

royalty-a payment made esp. to writers and musicians every time their books or songs are bought or used by others

shake out-to change over a period of time before a final result is known

constantly-continuously over a period of time; always.

adaptive-changing quickly to suit different conditions

server farm-another term for data centre

transcode-convert (language or information) from one form of coded representation to another , the process of changing a media file (= a file that contains sound and video) from one format (= the way in which information is arranged and stored on a computer) to another

## Captions and subtitles
>-to make video more accessible to every one add captions with `<track>` element and point to a text file. The video player will provide all the functionality so a viewer can turn captioning on and off or switch from one set of subtitles to another.  
-there are many file formats for captions. But on the web, we want to use webvtt, web video text tracks. It's basically a plain text file with a vtt extension and the time code information that tells the video player when to show each line.  
-to get these captions to show up on our video we put a `<track>` element inside the `<video>` element. On the `<track>` element, we'll use the `src` attribute to point to the .vtt subtitle file. We'll use the `kind` attribute to tell the browser that this is captions or subtitles. We'll add a `label` of english that will show up in the player as a label for this choice. We'll use a `srclang` attribute to specify which language this is. And we'll put a `default` attribute on this track element to specify that this track is the one we want to use by default when a user turns on captions. [original code example](https://codepen.io/jensimmons/pres/KKPevBe?editors=1100)
>```html
><video controls>
>  <source src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/moonwalk.480p.vp9.webm" 
>    type="video/webm">
>  <source src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/moonwalk.480p.h264.mp4" 
>    type="video/mp4">
> 
>  <track src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/moonwalk.vtt"
>         kind="captions"
>         label="English"
>         srclang="en"
>         default>
>
>   <track src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/moonwalk.es-la.es.vtt"
>         kind="subtitles"
>         label="Español"
>         srclang="es">
>  
>  <p>This would be a video of a moonwalk, if your device supported playing this video.</p>
></video>
>```
>NOTICE: The subtitles of above code snippet not be appeared on video player unless we add `crossorigin="*"` inside `<video>` tag. [check this issue for more info](https://github.com/imahdio/HTML-Essential-Training/issues/6)  
>NOTICE: Based on this lesson and [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/track) , there are several options for kind attribute includes:  
>* `captions` provides a transcription of audio.
>* `subtitles` provides translation of content.
>* `descriptions` provides descriptive information about what's happening visually in the video. This gives people the option of playing a track that reads aloud descriptions.  
>* `chapters` provides a text file that list the chapters in the video, giving users a way to jump from one section in the video to another.

>NOTICE: [*based my test and tries and this article*](https://act-rules.github.io/rules/ac7dc6) most assistive devices and screen readers not support `kind="descriptions"` attribute.  

accent-the way in which people in a particular area, country, or social group pronounce words

deaf-unable to hear, either completely or partly

bounce-to (cause to) move up or away after hitting a surface

## Embedding other media through iframes 
>-embedding is taking content from one site and placing it into the middle of a page on another site.  
-you can embed a map from Google or Mapbox or a code demo from CodePen or Glitch or a slide deck from Speaker Deck or Notist. It's common to embed something complex from a service that takes care of all the hard parts for you.  
-the iframe element has several attributes on it, including height and width.  Src is going to point to the source of the video file.  
-there are definitely some security considerations to be had about pulling in code from other sites.  If a bunch of different people are going to be entering content into a system, you're not going to want to just allow all iframes. Think about the security.  

likely-probably

white label product-It's a product or service produced by one company (the producer) that other companies (the marketers) rebrand to make it appear as if they had made it.
## Chapter Quiz
>-we can't create a video element that specifies diffrent resolutions of video that browsers can choose from when loading the video. Instead, the browser adapts to circumstances as needed. (*in my point of view this quotation is wrong because based what I learn from Video lesson without using adaptive bitrate streaming technology on server side , neither browser nor html element cannot switch between diffrent resolutions of video*)  
>-the following code snippet produces an audio player with control features.
>```html
><audio controls src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/birds.mp3"></audio>
>```
>-built in HTML video players do not permit adaptive bitrate streaming.  
>-Embed codes built with the iframe element make it easier combine content from other sources into your pages and apps.  

drawback-a disadvantage or the negative part of a situation

tedious-boring

