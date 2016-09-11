# &lt;juicy-checkbox-group&gt; [![Build Status](https://travis-ci.org/Juicy/juicy-checkbox-group.svg?branch=gh-pages)](https://travis-ci.org/Juicy/juicy-checkbox-group)

> Polymer element to create editable group of checkboxes.

## Demo

[Check it live!](http://Juicy.github.io/juicy-checkbox-group)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install juicy-checkbox-group --save
```

Or [download as ZIP](https://github.com/Juicy/juicy-checkbox-group/archive/gh-pages.zip).

## Usage

1. Import Web Components' polyfill, if needed:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/juicy-checkbox-group/juicy-checkbox-group.html">
    ```

3. Start using it!

    ```html
<juicy-checkbox-group editable name="{{model.Label}}">
      <template is="dom-repeat" items="{{model.CheckboxItems}}">
          <juicy-checkbox-group-item class="checkbox-item" index="{{index}}" position="{{item.Position}}" label="{{item.Label}}" checked="{{item.Checked}}" editable on-delete="onItemDelete"></juicy-checkbox-group-item>            
      </template>             
</juicy-checkbox-group>  
    ```

## juicy-checkbox-group properties

Name     | Options     | Default      | Description
---           | ---         | ---          | ---
`name`         | *string*    | -        | Label of the group
`namePlaceholder`         | *string*    | Type group name here | Label input placeholder, applies only if the group is in editing mode
`editable`         | *boolean*    | false | Switches group into editing mode (allows changing label)

## juicy-checkbox-group-item properties

Name     | Options     | Default      | Description
---           | ---         | ---          | ---
`position`         | *string*    | -        | Position of the item
`label`         | *string*    | -        | Checkbox item label
`checked`         | *boolean*    | false        | Determines if checkbox is checked
`checkable`         | *boolean*    | false        | Determines if checkbox can be checked (otherwise it's disabled)
`editable`         | *boolean*    | false        | Switches item into editing mode (allows changing label)
`placeholder`         | *string*    | Type item name here        | Label input placeholder, applies only if the item is in editing mode
`disableCheckbox`         | *boolean*    | false        | Determines if checkbox is available for editing


## Events

Event         | Description
---           | ---
`check` | Triggers when checkbox is checked.
`uncheck` | Triggers when checkbox is unchecked.
`checkboxLabelEditorEnter` | Triggers when enter is pressed inside checkbox item label editing field.
`delete` | Triggers when delete icon on the left of checkbox item is clicked.





## History

For detailed changelog, check [Releases](https://github.com/Juicy/juicy-checkbox-group/releases).

## License

MIT
