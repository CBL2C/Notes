# HTML Tables and Forms

## Tables
Tables are used to arrange content into rows and columns in a tabular format.  

**TABLES ARE GARBAGE.** ***PLEASE*** **DO NOT USE TABLES UNLESS YOU ABSOLUTELY HAVE TO.**
Tables are the spawn of Satan and are extremely difficult to style.  
**Save yourself your own sanity and don't use Tables if you can use literally any other option!**

### Basic Tables
```html
<table>                         // Opening the table element itself
    <thead>                     // The header on the table
        <tr>                    // Opening a row in the header
            <th>Numbers</th>    // Table header element, which holds the column name
            <th>Letters</th>    // Second table header element, which holds the second comumn name
        </tr>                   // Closing the row
    </thead>                    // Closing the table header
    <tbody>                     // Opening the table body
        <tr>                    // The first table row
            <td>1</td>          // The table data element, which holds an individual cell
            <td>A</td>          // Each additional row element is in a separate column
        </tr>                   // Closing the row
        <tr>                    // Second row
            <td>2</td>          // The table data elements for the second row
            <td>B</td>
        </tr>                   // Closing the row
        <tr>                    // Third Row
            <td>3</td>          // The table data elements for the third row
            <td>C</td>
        </tr>                   // Closing the row
        </tbody>                // Closing the table body
    </table>                    // Closing the table
```
<table>
    <thead>
        <tr>
            <th>Numbers</th>
            <th>Letters</th>
        </tr>
    </thead>
    <tbody>
        <tr>              
            <td>1</td>  
            <td>A</td>
        </tr>             
        <tr>              
            <td>2</td>    
            <td>B</td>
        </tr>
        <tr>
            <td>3</td>    
            <td>C</td>
        </tr>    
    </tbody>       
</table>    

<br>

### More Complex Tables
Sometimes, you may need a row or a column to span across multiple instances:

```html
<table>
        <tr>              
            <td rowspan="2">1</td>  
            <td>A</td>
        </tr>             
        <tr>         
            <td>B</td>
        </tr>
        <tr>    
            <td colspan="2">C</td>
        </tr>
        <tr>
            <td>2</td>
            <td>D</td>
        </tr>     
</table>    
```
<table>
        <tr>              
            <td rowspan="2">1</td>  
            <td>A</td>
        </tr>             
        <tr>         
            <td>B</td>
        </tr>
        <tr>    
            <td colspan="2">C</td>
        </tr>
        <tr>
            <td>2</td>
            <td>D</td>
        </tr>     
</table>   

<br>

## Forms
Forms allow users to submit data to a server and recieve information back.  

```html
<form>
    <input type="text">                 // Creates the text box 
    <input type="submit" value="go">    // Creates the submit button
</form>
```

<img src="../images/input_form.png">

However, this form above is only for show. It will not actually send user data to a server. 