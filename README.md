# UI-SELECT (UNDER CONSTRUCTION)
Simple and easy to use "Select", "Multiselect" and "Combobox" component

<br>

### HTML

```HTML
  
  <!-- generate a select -->
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


<br>

### GLOBAL ATTRIBUTES

<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th></th>
  </tr>
  <tr>
    <td>src</td>
    <td>
       Url that will be call by ajax to get more options
    </td>
    <td>src='/url/to/data?filter=%filter%'</td>
  </tr>
  <tr>
    <td>src-text</td>
    <td>
      Url that could be use to initialise text attribute of the initial value
    </td>
    <td>src='/url/to/text/data?filter=%filter%'</td>
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
    <td>name</td>
    <td>Used for form submission</td>
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


<br>

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
  <tr>
    <td>tokenSeparators</td>
    <td></td>
    <td></td>
  </tr>
</table>


<br>

### COMBO ATTRIBUTES

<table>
  <tr>
    <th>Attribute</th>
    <th>Description</th>
    <th></th>
  </tr>
  <tr>
    <td>not-empty</td>
    <td>Bring back last value if field is empty</td>
    <td><ui-combo not-empty></ui-combo></td>
  </tr>
</table>


<br>
  
### SRC URL RESPONSE


#### SIMPLE USE
```javascript
  [
    {"text":"some text", "value":"some value"},
    //...
  ]
```

#### INCLUDING A "SHOW MORE" OPTION
To add a "show more" options for the users, you can return an object with a <kbd>count</kbd> and <kbd>results</kbd> property. As long the count is lower than the total number of item shown, an item <kbd>show more</kbd> will be displayed at the bottom of the list. This will add <kbd>more=1</kbd> as a get parameter to the src url, the value of the parameter will be the number of times the <kbd>show more</kbd> was clicked (for the current research if your are not using the ui-select).

The src url should not return the same results as before but only the next results.

```javascript
  /* /some/url?search=someText */
  {
    "count":1337,
    "results":[
      {"text":"text 1", "value":"value 1"},
      {"text":"text 2", "value":"value 2"},
    ]
  }
  /* /some/url?search=someText&more=1 */
  {
    "count":1337,
    "results":[
      {"text":"text 3", "value":"value 3"},
      {"text":"text 4", "value":"value 4"},
    ]
  }
```

<br>

### DISABLING A DROPDOWN ELEMENT
To disable an element coming from an url, simple add the attribute <kbd>"disabled":"1"</kbd> in the definition.
To disable an element coming from <kbd>option</kbd> html tag, simply add the <kbd>disabled</kbd> attribute.

<br>

### CSS VARIABLES

<table>
  <tr>
    <th>Name</th>
    <th>Description</th>
    <th>default</th>
    <th>example</th>
  </tr>
  <tr>
    <td>--rgb-outline</td>
    <td>rgb params separated by comma representing the color of the outline</td>
    <td></td>
    <td>--rgb-outline: 0, 170, 255</td>
  </tr>
  <tr>
    <td>--rgb-outline-hover</td>
    <td>rgb params separated by comma representing the color of the outline(minus shadow) on hover, if not specified, it will use the outline color</td>
    <td></td>
    <td>--rgb-outline-hover: 0, 0, 0</td>
  </tr>
  <tr>
    <td>--ui-select-background-menu-hover</td>
    <td>rgb params separated by comma representing the color of the outline(minus shadow) on hover, if not specified, it will use the outline color</td>
    <td>#e2e2e2</td>
    <td></td>
  </tr>
  <tr>
    <td>--ui-select-background-menu-selected</td>
    <td>rgb params separated by comma representing the color of the outline(minus shadow) on hover, if not specified, it will use the outline color</td>
    <td>--ui-select-background-menu-hover</td>
    <td></td>
  </tr>
  <tr>
    <td>--ui-select-maximum-menu-height</td>
    <td></td>
    <td>250px</td>
    <td></td>
  </tr>
  <tr>
    <td>--ui-select-font-family</td>
    <td></td>
    <td>Roboto</td>
    <td></td>
  </tr>
</table>
