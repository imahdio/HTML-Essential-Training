# 09-Forms and Interactive Elements
## HTML form basics
> -Form fields have been an integral part of the web for decades. We log into sites , buy things , request a search, add content to a site through semantic form elements.  
-By using HTML `<form>` elements we tap into the power that's built into the browser ensure that our forms will work on every device.  
-`<input>` element has 2 diffrence with other elements:
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
>![image](https://user-images.githubusercontent.com/64577273/147369222-8ec9203d-24b0-48f6-a133-22e61a1b58f8.png)
>
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
## More on forms
>-`<type>` element define the type of input we want from fields. If you leave `<type>` off, as we did in the last lesson, the browser will assume that it's type of text.  
-with `type="email"` the browser will double-check, and see if the data that they entered is an email. if a user tries to type something that's not an email address, they get a warning, and are asked to fix it.  
-`type="submit"` tells the browser that our button is a submit button.  
-We can also add a `required` attribute, to make the email feel required. Now the browser will insist that the user fills out the email field, before the form can be submitted.  
-`placeholder` attribute could help users understand what they should fill into the field. We use the `placeholder` attribute, and put a suggestion, or an example. It's light gray by default. And as soon as I click into this field, the placeholder disappears. It's only a suggestion, it disappears.  
-`value` attribute make pre-populated fileds with real content. When I go to type my own email address in here, the suggested one is in the way. I have to manually erase it to put in my own.  
-[Check the complete Code snippet in here](moreOnForms.html)

fill out-to write or type information in spaces that are provided for it

placeholder-a symbol or piece of text in a mathematical expression or computer instruction that can be replaced by particular pieces of information

prepopulated-If you are referring to a form (like a survey or application), it means that information has already been filled in.

frictionless-effortless,smooth

integrated-combined to form a single thing
## Additional form element types
>-we can use proper semantic HTML elements in our forms and style them with a custom look and feel by adding CSS.  
-Password, search, and phone number fields are very similar in structure to the text and email form fields, but I've changed the type.  
-Notice: Users should not fill out forms like this on sites that haven't been secured by HTTPS. Especially not a password field. otherwise the browser is warning us not to use this, that's because this page is set up to use HTTP and not HTTPS.  
-Notice: The phone number field will prompt many devices to provide a telephone pad for the keyboard which makes sense when entering a phone number.  
-`<textarea>` element get a paragraph or whole article of text. It's similar to the input element, and we pair it with a label in the same way, but it is a different element. We can put a size on text area using the cols and rows attribute, but we don't have to, frequently we use CSS to override this size anyway. You'll notice there's a scroll bar that appears when the box is full of content, and there's little handle in the corner that lets the user resize the box.  
-`date`, `color`, and `file` are three more input types to our form. I've set `type="date"` for the `date` field. `type="color"` for color and `type="file"` for the file field.  
-`accept="image/*"` attribute in `file` element , limits the kinds of files that are acceptable to images only and `accept="image/png, image/gif, image/jpeg"` limits the kinds of files that are acceptable to png , jpg and gif.  
-`multiple` attribute in `file` element allow multiple files selection.  
-The `date` input type provides a convenient interface for setting a date.
>```html
><label for="date">Date</label>
><input id="date" name="date" type="date">
>```
>![image](https://user-images.githubusercontent.com/64577273/147383216-43432a51-194c-4f0f-b3b3-184e16243b43.png)  
>-The color field opens a color picker. This is an operating system or browser based color picker wheel.  
>![image](https://user-images.githubusercontent.com/64577273/147383271-d77bb5cf-56a2-438a-a9a2-0d86f0b8f0f7.png)  
>-File provides an interface for uploading a file, and you can see that because of `accept="image/*"` attribute , it will let me pick only image files, but not any other files.  
>-For a simple checkbox, we use a label and input again, this time with a type of checkbox. `checked` attribute tells the browser this box is checked by default. if give the checkbox input a value, so that when the form is submitted, it has value to pass along.  
>-We can make a drop-down list called a select list, using the select and option elements. 
> ```html
> <div>
>     <label for="selectlist">Choose one</label>
>     <select id="selectlist" name="selectlist">
>         <option>First Option</option>
>         <option>Second Choice</option>
>         <option>Third Thing</option>
>     </select>
> </div>
> ```
>![image](https://user-images.githubusercontent.com/64577273/147384302-3e613e77-3965-4d1c-8d79-f606d7b88c6d.png)  
>-To make a set of checkbox, or a set of radio buttons, I've set the type to checkbox or radio, I've also wrapped their labels and input elements in what's called a fieldset with a legend.
> ```html
> <fieldset>
>     <legend>Checkbox fields inside a fieldset</legend>
>     <input id="thischeck" name="checkboxlist" type="checkbox" value="This" checked >
>     <label for="thischeck">This</label>
>     <input id="orcheck" name="checkboxlist" type="checkbox" value="And Or">
>     <label for="orcheck">And/Or</label>
>     <input id="thatcheck" name="checkboxlist" type="checkbox" value="That">
>     <label for="thatcheck">That</label>
> </fieldset>
> 
> <fieldset>
>     <legend>Radio button list inside a fieldset</legend>
>     <input id="thisradio" name="radiobutton" type="radio" value="This" checked>
>     <label for="thisradio">This</label>
>     <input id="orradio" name="radiobutton" type="radio" value="Or">
>     <label for="orradio">Or</label>
>     <input id="thatradio" name="radiobutton" type="radio" value="That">
>     <label for="thatradio">That</label>
> </fieldset>
> ```
>-[Check the complete Code snippet in here](additionalFormElementTypes.html)

`<legend>` Tag-The legend elements are the parent element. This tag is used to define the caption for the `<fieldset>` element.
## Chapter Quiz
>-by specifying the `type` attribute , we can require a certain format for data entered into an `<input>` element.  There are many types, including telephone numbers, dates, names, and others.  
-The label element provides easier access to the form field, but has nothing to do with type attributes.  
-to have maximum versatility and robustness with minimum effort , use `<form>` elements instead of custom coding data inputs in JavaScript. Substantial effort has already been spent on form elements and their use with different display types.  
-when you put a `<label>` element around an `<input>` element , Clicking on the label activates that form field, and screen readers know that the label goes with the field.  
-a `placeholder` is a temporary suggestion of form, while a `value` is an estimate of the correct response.  
-The value attribute fills the field with a value that will be submitted with the form. The placeholder shows a suggestion, but doesn't really enter it. only use value if you want that value to go to the server unless the user changes it explicitly.

extensively-to a large or detailed degree

tailor-to adjust something to suit a particular need or situation

versatility-ability to adapt or be adapted to many different functions or activities

substantial-large in size, value, or importance