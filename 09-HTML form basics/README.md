# 09-HTML form basics
## HTML form basics
> -Form fields have been an integral part of the web for decades. We log into sites , buy things , request a search, add content to a site through semantic form elements.  
-By using HTML `<form>` elements we tap into the power that's built into the browser ensure that our forms will work on every device. -`<input>` element has 2 diffrence with other elements:
> 
> 1. because this element is so old it doesn't have the same structure as the more modern elements and we don't close this element.
> 2. the input element is what's called a replaced element, meaning it's a kind of marker for the browser that tells the browser, hey, go get one of those piles of functionality that you have and stick it here.
>
>-here is simple form that people might use to sign up for an email newsletter. the next 4 notices have explained the code functionality in details.
> ```html
> <!doctype html>
> <html dir="ltr" lang="en-us">
>   <head>
>     <title>Form Basics</title>
>     <meta charset="utf-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1">
>     <link rel="stylesheet" href="space.css">
>   </head>
> 
>   <body>
>     <main>
> 
>     <form action="success.html" method="get">
>         <label for="name">Name</label>
>         <input name="name" id="name">
>         <label for="email">Email</label>
>         <input name="email" id="email">
> <br>
>         <label>Name <input name="name"></label>
>         <label>Email<input name="email"></label>
> 
>         <button>Sign up</button>
>     </form>
> 						
>   </main>
>   </body>
> </html>
> ```
>-Notice 1: the `action` and `method` attributes hook the form up to some kind of backend to give the form some place to go & some method by which to send the data.  
-Notice 2: using `method="get"` is not a recommended practice for a real website. It's super insecure. But it works for the purpose of making a demo.  
-Notice 3: the `input` fields need proper `name` attribute to report the data that's been entered into the form.  
-Notice 4: there are 2 ways for tying `<label>` and `<id>` attributes together.
> 1. we can add a `for` attribute to the label and add an `id` to the input with a matching name.
> 
> ```
> <label for="email">
>     Email
> </label>
> 
> <input name="email_address" id="email"></input>
> ```
> 
> 2. we could wrap the `<label>` around the outside of the `<input>`, which clearly communicates to the browser, hey, this label is for this input field.
> 
> ```
> <label>
>     Email
>     <input name="email_address"></input>
> </label>
> ```
> 
> Notice: as result of above code snippet , by clicking on the label , the focus jumps to the right input element. we do it , because many people who won't be able to use the form if we don't connect the label to the input element.

integral-necessary and important as a part of a whole

tap into sth-to manage to use something in a way that brings good results

profoundly-(of a person or statement) having or showing great knowledge or insight ; (of a state, quality, or emotion) very great or intense

hook sth up-to connect two things

promise-to tell someone that you will certainly do something

tie-to fasten together two pieces of string or other long, thin material, or to hold together with string, rope, etc.

tie together-fasten , join

ton-a lot

leverage-to use something that you already have in order to achieve something new or better