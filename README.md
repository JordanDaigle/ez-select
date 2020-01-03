# ui-select
Simple and easy to use "Select", "Multiselect" and "Combobox" component

# UNDER CONSTRUCTION

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

<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th></th>
  </tr>
  <tr>
    <td>src</td>
    <td>url that will be call by ajax to get more options</td>
    <td>src='/url/to/data?term=%value%'</td>
  </tr>
  <tr>
    <td>not-empty</td>
    <td>bring back last value if field is not empty</td>
    <td><ez-combo not-empty></ez-combo></td>
  </tr>
  <tr>
    <td>text</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>value</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>onchange</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>autosort</td>
    <td>automatically sort options shown</td>
    <td></td>
  </tr>
</table>





