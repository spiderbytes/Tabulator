![Tabluator Table](http://olifolkerd.github.io/tabulator/images/tabulator.png)

### Version 3.1 Out Now!

An easy to use interactive table generation plugin for JQuery UI

Full documentation & demos can be found at: [http://olifolkerd.github.io/tabulator](http://olifolkerd.github.io/tabulator)
***
![Tabluator Table](http://olifolkerd.github.io/tabulator/images/tabulator_table.jpg)
***
Features
================================
Tabulator allows you to create interactive tables in seconds from any HTML Table, Javascript Array or JSON formatted data.

Simply include the library and the css in your JQuery UI project and you're away!

Tabulator is packed with useful  features including:

- Fully CSS styleable
- Virtual DOM
- JSON, array or AJAX data loading
- Column sorting
- Column Freezing
- Responsive Layout
- Pagination
- Editable cells
- Data Accessors and Mutators
- Adding/Deleting rows
- Custom data formatting
- Movable rows and columns
- Persistant Column Layouts (storage of table layout changes between page loads)
- Grouping Rows
- Data filtering
- Resizable columns
- Auto scaling  to fit data/element
- Many theming options
- Custom click and context Events
- Callbacks at every stage of data processing and rendering


Setup
================================
Setting up tabulator could not be simpler.

Include the library and the css
```html
<link href="dist/css/tabulator.min.css" rel="stylesheet">
<script type="text/javascript" src="dist/js/tabulator.min.js"></script>
```

Create an element to hold the table
```html
<div id="example-table"></div>
```

Turn the element into a tabulator with some simple javascript
```js
$("#example-table").tabulator();
```


### Bower Installation
To get Tabulator via the Bower package manager, open a terminal in your project directory and run the following commmand:
```
bower install tabulator --save
```

### NPM Installation
To get Tabulator via the NPM package manager, open a terminal in your project directory and run the following commmand:
```
npm install jquery.tabulator --save
```

### CDNJS
To access Tabulator directly from the CDNJS CDN servers, include the following two lines at the start of your project, instead of the localy hosted versions:
```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/tabulator/2.11.0/tabulator.min.css" rel="stylesheet">
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/tabulator/2.11.0/tabulator.min.js"></script>
```

Coming Soon
================================
Tabulator is actively under development and I plan to have even more useful features implemented soon, including:

- Multi-level row grouping
- multi dimentional data handling
- Data Reactivity
- Custom Row Templates
- Additional Editors and Formatters
- Column Calculations
- Copy to Clipboard
- Print Styling
- Drag Rows Between Tables

Get in touch if there are any features you feel Tabulator needs.