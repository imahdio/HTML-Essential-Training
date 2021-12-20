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

