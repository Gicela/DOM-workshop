# Manipulating the DOM (Object Document Model)

The DOM is a tree of JavaScript node objects.

Open the Web Developer Tools in your browser and open the console.

## Writing to the DOM

### create a strong element and write it to the DOM
`document.getElementById('A').innerHTML = '<strong>Hello World</strong>';`

### Create a DIV element and text node to replace the span tag.
`document.getElementById('B').outerHTML = '<div id ="B"> What's up</div>';`

### Add some text to div #C
`document.getElementById('C').textContent = 'New content';`

### Create a text node and update div #D
`document.getElementById('D').innerText = 'Updated content';`

### Create two element nodes
`var elementNode = document.createElement('strong')`
`var textNode = document.createTextNode('This text is strong')`

### Append the elementNode and textNode to the DOM
`document.querySelector('p').appendChild(elementNode)`
`document.querySelector('strong').appendChild(textNode)`

### Log all the HTML inside <body>
`document.body.innerHTML`

### Create two element nodes
`var li = document.createElement('li')`
`var text = document.createTextNode('Apples');`
`li.appendChild(text)`

### Append the li and text nodes to the DOM

`ul = document.querySelector('ul')`
`ul.insertBefore(li, ul.firstChild)`

### Remove a child from its parent node

`divA = document.getElementById('A')`
`divA.parentNode.removeChild(divA)`
### Log document.body.innerHTML

### Replace an element node
`var divA = document.getElementById('A')`
`var span = document.createElement('span')`
`span.textContent = "Replacing text for DIV with #A"`
`divA.parentNode.replaceChild(span, divA)`

### Replace a text node

`var divB = document.getElementById('B')`
`var newBText = document.createTextNode('New text for div #E')`
`divB.parentNode.replaceChild(newBText, divB)`

### Traversing the DOM

`Find the first & last child of the UL`
`var ul = document.querySelector('ul')`
`ul.firstElementChild.nodeName`
`ul.lastElementChild.nodeName`

### Find the next & previous sibling of the UL
`ul.nextElementSibling.nodeName`
`ul.previousElementSibling.nodeName`

### DOM Events
`divA = document.getElementById('A')`
`divA.onclick = function(){
	console.log('You clicked me!')
}`