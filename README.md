autocomplete
============

An jQuery library, autocomplete.js. It can be used as a select drop-down menu and also for ajax auto-complete etc. And also you can do a lot more with this light jQuery library js.


Dependecies
------------
The only requirement for jquery-autocomplete is jQuery. No other plugins are required.


Version
----
1.0


Usage
-----
##### Add the following scripts to your html page

* jQuery.js
* autocomplete.js

```html
<script type="text/javascript" src="path/to/jQuery.js"></script>
<script type="text/javascript" src="path/to/autocomplete.js"></script>
```

##### Initialization



```html
$('input-element').autocomplete(options)
```


Options
-------
This options are default:

```js
{
    data: [],
    //Data those are to be displayed in the dropdown list. 
    //Data has to be passed as a array.
    height: '',
    //e.g '100px'
    //Height of the dropdown. Default will make th height so as to contain all 
    //values without collision
    width: '',
    //[100px|100|100em|100%...]
    //Width of the dropdown.
    //default width will take the width of the input box.
    sort: true,
    //[true|false],
    //if sort true the the sorted input array will be displayed in th dropdown
    //if false arrayis data displayaed as it is given
    searchIndex: -2,
    //[-2|-1|0|1|2...]
    //searchIndex used for searching filetring data in auto-complete
    //-2: filer data if the searched string is a substring
    //-1: filter data which doesn't contain the search string
    //n (0,1,2...): filter data which contains the searched string starting from index n
    staticData: null,
    //e.g [Sample text|<button>Click me</button>...}
    //statisc data is displayed in the dropdown irrespective of a match or not.
    //static data can be both text and html
    //as static data is rendered repeatedly hence any event regd with this data may lost
    //but you can add inline javascript event lestener(onclick, onmouseover etc)
    matchType: 'caseinsesitive',
    //[caseinsesitive|casesensitive]
    //case is considered dependong upon this variable while matcihng string
    allowDuplicate: false
    //[true|false]
    //whether to allow duplicate data field.
}

```


Methods
-------
The methods can be applied to a autocomplete object as below:

```js

var autoComp = $('input-element').autocomplete(options);

autoComp.getData()
//gets the current data of autocomplete object has
autoComp.setData(data)
//sets current data of autocomplete object
autoComp.setOptions(options)
//sets current options of autocomplete object
autoComp.addData(data)
//appends data to existing data of autocomplete object
autoComp.getListElement()
//returns the dropdown element of autocomplete object
autoComp.getStaticData()
//returns static data of autocomplete object
autoComp.setStaticData(staticData)
//sets static data of autocomplete object
autoComp.getLastValue()
//returns last selected value of autocomplete object
autoComp.getValue()
//returns current value of input field
autoComp.setValue(val)
//sets input field value
autoComp.showList()
//force show the dropdown
autoComp.hideList()
//force hide the dropdown
autoComp.rebuildList()
//refreshes content of dropdown list
autoComp.destroy()
//destroys autocomplete object
```
