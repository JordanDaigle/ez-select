# ui-select
Simple and easy to use "Select", "Multiselect" and "Combobox" component

## UNDER CONSTRUCTION


<br><br>
### HTML

```HTML
  
  <!-- generate a select following the design of the combo // multiselect -->
  <ui-select name='my-select'>
    <option selected value='value1'>text1</option>
    <option value='value2'>text2</option>
    <option value='value3'>text3</option>
  <ui-select>
  
  <!-- generate a combobox -->
  <ui-combo name='my-combo' src='/url/to/extra/option' value='initialValue' text='initialText' not-empty>
    <option selected value='value1'>text1</option>
    <option value='value2'>text1</option>
    <option value='value3'>text1</option>
    <option value='value4'>text1</option>
  </ui-combo>
  
  <!-- generate a multiselect -->
  <ui-multiselect name='my-multiselect' src='/url/to/extra/option' value='initialValue' text='initialText'>
    <option selected value='value1'>text1</option>
    <option value='value2'>text1</option>
    <option value='value3'>text1</option>
    <option value='value4'>text1</option>
  </ui-multiselect>
  
```


<br><br>
### Global ATTRIBUTES

<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th></th>
  </tr>
  <tr>
    <td>src</td>
    <td>Url that will be call by ajax to get more options</td>
    <td>src='/url/to/data?term=%text%'</td>
  </tr>
  <tr>
    <td>src-text</td>
    <td>Url that could be use to initialise text attribute of the initial value</td>
    <td>src='/url/to/text/data?term=%value%'</td>
  </tr>
  <tr>
    <td>value</td>
    <td>initial value</td>
    <td></td>
  </tr>
  <tr>
    <td>text</td>
    <td>initial text</td>
    <td></td>
  </tr>
  <tr>
    <td>onchange</td>
    <td>handle change event</td>
    <td></td>
  </tr>
  <tr>
    <td>autosort</td>
    <td>automatically sort options shown</td>
    <td></td>
  </tr>
</table>


<br><br>
### SELECT ATTRIBUTES

<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th></th>
  </tr>
</table>


<br><br>
### MULTISELECT ATTRIBUTES

<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th></th>
  </tr>
  <tr>
    <td>tags</td>
    <td>Allow user to create items</td>
    <td>
        Setting only "tags" attribute will set the value the same as the text.
        <br>
        If a value is setted into the attribute, it will be used as the default value
    </td>
  </tr>
</table>


<br><br>
### COMBO ATTRIBUTES

<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th></th>
  </tr>
  <tr>
    <td>not-empty</td>
    <td>Bring back last value if field the is empty</td>
    <td><ui-combo not-empty></ui-combo></td>
  </tr>
</table>


<br><br>
### CSS VARIABLES

<table>
  <tr>
    <th>Name</th>
    <th>Description</th>
    <th>example</th>
  </tr>
  <tr>
    <td>--rgb-outline</td>
    <td>rgb params separated by comma representing the color of the outline</td>
    <td>--rgb-outline: 0, 170, 255</td>
  </tr>
  <tr>
    <td>--rgb-outline-hover</td>
    <td>rgb params separated by comma representing the color of the outline(minus shadow) on hover, if not specified, it will use the outline color</td>
    <td>--rgb-outline-hover: 0, 0, 0</td>
  </tr>
</table>
