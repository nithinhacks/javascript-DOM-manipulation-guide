
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

```javascript
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

```javascript
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
| console.log(document.getElementsByTagName('name of the tag')) | gets the element with the given tag name |


```javascript
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

## QUERYSELECTOR

| Command | Description |
| --- | --- |
| console.log(document.querySelector('any css selector')) | gets the first css selector given |


```javascript
    usage examples:
        var header = document.querySelector('#main-header');
        header.style.borderBottom = 'solid 4px #ccc'; // adds style to given css selector

        var input = document.querySelector('input');
        input.value = 'Hello World'; 

        var item = document.querySelector('.list-group-item');
        item.style.color = 'red'; // changes the color of first item in list-group-item class

        var lastItem = document.querySelector('.list-group-item:last-child');
        lastItem.style.color = 'blue'; // changes the color of the last item in list-group-item class

        var secondItem = document.querySelector('.last-group-item:nth-child(2)');
        secondItem.style.color = 'coral'; // changes the color of the second item in list-group-item class
```

## QUERYSELECTORALL

| Command | Description |
| --- | --- |
| console.log(document.querySelectorAll('any css selector'))  | gets all the elements of given css selector |


```javascript
    usage examples:
        var titles = document.querySelectorAll('.title');
        console.log(titles); // gets all elements with class title
        titles[0].textContent = 'Hello'; // changes the textcontent of first element with class title

        var odd = document.querySelectorAll('li:nth-child(odd)'); // gets all the odd elements of the given css selector
        var even = document.querySelectorAll('li:nth-child(even)'); // gets all the even elements of the given css selector 

        for(var i=0; i<odd.length; i++)
        {
            odd[i].style.backgroundColor = '#f4f4f4'; // changes the color of all odd elements
            even[i].style.backgroundColor = '#ccc'; // changes the color of all even elements
        }
```