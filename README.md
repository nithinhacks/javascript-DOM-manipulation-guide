
# javascript DOM manipulation

basic guide for javascript document object model manipulation


## Author

- [@nithinhacks](https://github.com/nithinhacks)


  
## EXAMINE THE DOCUMENT OBJECT

| Command | Description |
| --- | --- |
| console.dir(document) | gets all the document properties |
| console.log(document.domain) | gets the domain of the site |
| console.log(document.URL) | gets the URL of the site |
| console.log(document.title) | gets the title of the site |
| console.log(document.doctype) | gets the doctype |
| console.log(document.head) | gets the head of the site |
| console.log(document.body) | gets the body of the site |
| console.log(document.all) | gets everything in the html DOM |
| console.log(document.all[10]) | gets the 10th element in the html DOM |
| console.log(document.forms) | gets all the collection of forms |
| console.log(document.forms[0]) | gets the 1st form in the html DOM |
| console.log(document.links) | gets all the collection of links |
| console.log(document.images) | gets all the images in the html DOM |


## GETELEMENTBYID

| Command | Description |
| --- | --- |
| console.log(document.getElementById('name of the ID')) | gets the element with the given ID |

```bash
    usage examples:
        var headertitle = document.getElementById('name of the ID');
        console.log(headertitle); // gets the content within the given ID
        console.log(headertitle.textContent); 
        // gets the text inside the given ID irrespective of the style applied (textContent)
        console.log(headertitle.innerText); 
        // gets the text inside the given ID with respective of the style applied (innerText)
        headertitle.innerHTML = '<h3>Hello</h3>';
        // adds h3(html) inside the given ID (innerHTML)
        headertitle.style.borderBottom = 'solid 3px #000';
        // used to modify the style for the given ID (style)
```

## GETSELEMENTSBYCLASSNAME

| Command | Description |
| --- | --- |
| console.log(document.getElementsByClassName('name of the class')) | gets the element with the given classname |

```bash
    usage examples:
        var items = document.getElementsByClassName('name of the class');
        console.log(items); // gets all the elements of the given class
        console.log(items[0]); // gets the first element of the given class
        items[0].textContent = 'Hello'; // adds text to the given class
        items[0].style.fontWeight = 'bold'; // changes the style of the given class
        items.style.backgroundColor = 'green'; // gives error
        
        // correct way 
        for(var i=0; i<items.length ; i++)
        {
            items[i].style.backgroundColor = 'green';
        }
```

## GETELEMENTSBYTAGNAME

| Command | Description |
| --- | --- |
| console.log(getElementsByTagName('name of the tag')) | gets the element with the given tag name |


```bash
        usage examples:
            var li = document.getElementsByClassName('name of the class');
            console.log(li); // gets all the elements of the given tag
            console.log(li[0]); // gets the first element of the given tag
            li[0].textContent = 'Hello'; // adds text to the given tag
            li[0].style.fontWeight = 'bold'; // changes the style of the given tag
            li.style.backgroundColor = 'green'; // gives error
            
            // correct way 
            for(var i=0; i<li.length ; i++)
            {
                li[i].style.backgroundColor = 'green';
            }
```