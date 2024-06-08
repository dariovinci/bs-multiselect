<h1>BS MULTISELECT</h1>
A light and simple multi select for bootstrap 5. If you like it you can support my work buying me a cofee: https://buymeacoffee.com/dariovinci


<h3>HOW TO USE IT</h3>

Wrap an input (an optionally a label) field in a div and choose an id. Example: multiselect-test

```html
<div id="multiselect-users-wrapper">
    <input type="text" class="form-control">
    <label for="multiselect-users">Utenti</label>
</div>
```

You can also use bs-multiselect with form floating. Example:
                
```html
<div id="multiselect-test">
    <div class="form-floating">
        <input type="text" class="form-control">
        <label for="multiselect-users">Utenti</label>
    </div>
</div>
```

Then in your js file add:

```js
const multiselect_test = new BsMultiselect({
  inputId: '#multiselect-test',
  dataArray: [],
  selectAll: true,
  showCompactSelection: true,
  maxHeight: 200px,
  showSearchBox: true,
});
```

<h3>OPTIONS</h3>
<table style="width:100%;">
  <thead>
    <tr>
      <td>OPTION</td>
      <td>VALUE</td>
      <td></td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>inputId</td>
      <td></td>
      <td>Id of the dig wrapping the input field</td>
    </tr>
    <tr>
      <td>dataArray</td>
      <td>[{
			'value': '1',
			'text': 'Option 1'
		}, {
			'value': '2',
			'text': 'Option 2'
		}</td>
      <td>dataArray is an array of obcjects where the first key pair is the checkbox value and the second key pair is the text you want to display</td>
    </tr>
    <tr>
      <td>selectAll</td>
      <td>(boolean) true/false</td>
      <td>Set true if you want to select all the option on init</td>
    </tr>
    <tr>
      <td>showCompactSelection</td>
      <td>(boolean) true/false</td>
      <td>Set true to display a compact view when there are 2+ selected options</td>
    </tr>
    <tr>
      <td>maxHeight</td>
      <td>(text)200px</td>
      <td>Set the max height of the dropdown menu</td>
    </tr>
    <tr>
      <td>showSearchBox</td>
      <td>(boolean) true/false</td>
      <td>Set true to display a search box to easily filter your select options</td>
    </tr>
    <tr>
      <td>ajaxSourceUrl</td>
      <td>url</td>
      <td>Url that will be used to fetch your options. Use only if dataArray is not defined and make sure that the response has the correct structure (like dataArray)</td>
    </tr>
  </tbody>
</table>

<h3>METHODS</h3>

<table style="width:100%;">
  <thead>
    <tr>
      <td>METHOD</td>
      <td></td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>getselectedItems()</td>
      <td>Returns an array of object with the same structure of dataArray defined at config</td>
    </tr>
    <tr>
      <td>getselectedItemsValues()</td>
      <td>Returns an array ot the selected values</td>
    </tr>
    <tr>
      <td>setSelectedElements(valuesArray, checked)</td>
      <td>valuesArray: array of value to select/deselect. checked: (boolean) true/false </td>
    </tr>
    <tr>
      <td>updateOptionsList(dataArray)</td>
      <td>Replace options with new ones</td>
    </tr>
    <tr>
      <td>reset()</td>
      <td>Reset the multiselect to the deafault state.</td>
    </tr>
    </tbody>
</table>

