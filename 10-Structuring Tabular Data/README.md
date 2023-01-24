# 10-Structuring Tabular Data
## When to use tables
>-you have to use HTML table for tabular data absolutly.  
-The whole point of semantic HTML is to tell computers everywhere what the thing you have is. If you have a button, use the button element. If you have a table, use the table elements.   
-what you should not do is misuse HTML table elements and pretend that you're making a table when you're not.  
-a long time ago, when we did not have CSS or any proper tools for styling or laying out our content on a web page, people used to take their content, break it up into a lot of little pieces, and jam all those pieces into the cells of an HTML table, and just pretend everything was okay **just like what occures nowdays in Html emails**. Things maybe looked okay or even good but the semantics were terrible.  
-we only should use Html tables for tabular data. tables are for such things like:
>* a chart of data from a research project, that's a table.
>* a bunch of information that's best communicated by aligning things into rows and columns, that's a data table.
>* comparing prices of things that are for sale, population data by town, election results, product comparisons, schedules, bits of information collected that you want people to be able to quickly compare.
>
>-as long as there's a semantic reason for the data to be organized into a table, use a table in HTML to semantically mark it up as what it is.    
-you can use CSS to rearrange how a table is displayed so it might not always look like a traditional table. Especially, perhaps, for small screens. Changing the layout for different sized screens.

somewhere along the way-at some point in time

evil-morally bad, cruel, or very unpleasant

tabular-arranged in rows and columns, in the form of a table

pretend-behave so as to make it appear that something is the case when in fact it is not

sore-upset and angry

scramble-move quickly in a disorganized fashion; When you scramble a message, it can no longer be read

Messy-untidy, disorganized

typeset-to arrange printed text and images on the page when preparing a book, newspaper, etc. for printing

headline-*based on the context and in my point of view* website layout

break sth up-to divide into many pieces, or to divide something into many pieces

jam-squeeze or pack tightly into a specified space

horrible-very shocking and frightening, very unpleasant

lay out something-to arrange in a pattern or design

population data-a set of individuals who share a characteristic or set of these, a population is mainly determined by geographies, such as all people in California, or all people in the United States

town-a place where there are a lot of houses, stores, and other buildings which is smaller than a city

reveal-to make known or show something that is surprising or that was previously secret
## Building table rows
> -To create an HTML table, you use several different HTML elements in just the right combination. `<table>`, `<tr>`, `<th>`, and `<td>`.
> 
>Element|Name|Purpose|Attributes
>-|-|-|-
>`<table></table>`|table|wraps the whole table|
>`<tr></tr>`|tr-table row|wraps around a set of elements,defining them as belonging to the same row|colspan,rowspan,headers
>`<th></th>`|th-table header|defines a header for a column|colspan,rowspan,scope
>`<td></td>`|td-table data|marks the actual bits of data|
>
> -[This table code snippet](https://codepen.io/imahdio/pen/mdjxRqr) has six rows, five rows about five different birds, and a top row, which contains the header for each column.
> 
> 1. we start with a `<table>` element to mark the beginning of the table. Of course we'll close it at the end, so let's do that now with `</table>`.
> 
> ```html
> <table>
> 
> </table>
> ```
> 
> 2. six pairs of `<tr>` and `</tr>` make six rows. five rows about five different birds, and a top row, which contains the header for each column.
> 
> ```html
> <table class="styled">
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
> </table>
> ```
> 
> 3. we'll put the content inside of each row. Let's start with the American goldfinch row like this:
> 
> ```html
> <table class="styled">
>     <tr>
>     </tr>
>     <tr>
>         <td>American Goldfinch</td>
>         <td>yellow</td>
>         <td>Mostly seeds.</td>
>         <td><img src="https://s.cdpn.io/10558/american-goldfinch.jpg" alt="american-goldfinch" width="360" height="261"></td>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
> </table>
> ```
> 
> 4. we put the content for the header in the first row, wrapping each one in a `<th>` element instead of a `<td>` element.
> 
> ```html
> <table class="styled">
>     <tr>
>         <th>Bird</th>
>         <th>Color</th>
>         <th>Diet</th>
>         <th>Photo</th>
>     </tr>
>     <tr>
>         <td>American Goldfinch</td>
>         <td>yellow</td>
>         <td>Mostly seeds.</td>
>         <td><img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/10558/american-goldfinch.jpg" alt="american-goldfinch" width="360" height="261"></td>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
>     <tr>
>     </tr>
> </table>
> ```
> 
> 5. the header is typeset in all caps, but I don't want the words to actually be in all caps. They aren't acronyms, so I'm putting them into my HTML as normal words, and using CSS to change how they look.
>
>-that's the basics of an HTML table, the `<table>` element, `<tr>` for table rows, `<th>` to mark content that's in a header, and `<td>` for marking up the content of each table cell.

shape up-to develop , to improve your behavior or performance

acronym-an abbreviation consisting of the first letters of each word in the name of something, pronounced as a word

row span-it specifies the number of rows a cell should span. That is if a row spans two rows, it means it will take up the space of two rows in that table
## Chapter Quiz
>-tables are the preferred option for creating layouts in HTML email because the other better options are not supported.  
-this code snippet produces the following image.  
>```html
><table class="styled">
>  <tr> <th> Name </th> <th> Phone </th> </tr>
>  <tr> <td> Bill LaVarre </td> <td> 555-2987 </td> </tr>
>  <tr> <td> Waymon LaVarre </td> <td> 555-4673 </td> </tr> 
></table>
>```  
>![image](https://user-images.githubusercontent.com/64577273/147405626-0b31ccf6-63ed-41ca-86fe-2b94c7167fa7.jpg)  
-The `<td>` element is usually nested in the `<table>` element and also in a `<tr>` element.