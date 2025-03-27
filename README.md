# adapt-tableadvanced 
A presentation component that displays a table. Each table cell can contain text and / or a graphic. For better mobile support, the table can have a fixed width. Users can pan the table horizontally. 

![adapt-tableadvanced](https://github.com/DeSimoD/sharedAssets/blob/main/screenshot_adapt-tableadvanced.png?raw=true)   

## Installation
To install the component with the [Adapt CLI](https://github.com/adaptlearning/adapt-cli), run the following from the command line:  
`adapt install adapt-tableadvanced`

Alternatively, this component can also be installed by adding the following line of code to the *adapt.json* file:  
`"adapt-tableadvanced": "*"`  
Then running the command:  
`adapt install`  
(This second method will reinstall all plug-ins listed in *adapt.json*.)  

Use the [Plug-in Manager](https://github.com/adaptlearning/adapt_authoring/wiki/Plugin-Manager) to use this component in the Adapt authoring tool.

## Settings Overview
A properly formatted JSON is available in [*example.json*](https://github.com/DeSimoD/adapt-tableadvanced/blob/master/example.json)
  
### Row / Column as headings
Use the `_rowHeaderIndexes` and `_colHeaderIndexes` attributes to set a row or column as a heading. Multiple indexes must be seperated with `,`.
```json
"_rowHeaderIndexes": "0,4",
"_colHeaderIndexes": "0",
```

### Table min width
You may define a min width for the table in pixel.   
`_minWidth`    

### Remove double borders
Double borders can occur because both the table and the `<th>` and `<td>` elements have separate borders. To remove double borders enable this option.
```json
"_isBorderCollapse": true,
```

### Table border appearance
Defines the appearance of the table border. The default appearance is `solid`.
```json
"_tableBorderAppearance": "solid",
```

### Table border line width
Thickness of the table border line in pixels.
```json
"_tableBorderLineWidth": 3,
```

### Rows
Each row can have a css class and a list of cells.  

#### Cells

##### column / row span 
Wrapps html [colspan](https://www.w3schools.com/tags/att_td_colspan.asp) and [rowspan](https://www.w3schools.com/tags/att_td_rowspan.asp) attribute.  

##### Cell border appearance
Defines the appearance of the cell border. The default appearance is `solid`
```json
"_cellBorderAppearance": "solid",
```

##### Cell border line width
Thickness of the cell border line in pixels.
```json
"_cellBorderLineWidth": 1,
```

##### Background color
Background color of the cell as a valid css value.
```json
"_cellBackgroundColor": "darkgreen",
```

##### Text color
Text color of the cell as a valid css value.
```json
"_cellTextColor": "white",
```

##### text / graphic 
Text and or graphic content of the table cell. 

##### Horizontal alignment
Defines the horizontal alignment in the cell. `Left`: The contents of the cell are left-aligned. `Center`: The contents of the cell are centered. `Right`: The contents of the cell are right-aligned. The default alignment is `center`.
```json
"_textAlignment": "center",
```

##### Vertical alignment
Defines the vertical alignment in the cell. `Top`: Allign content to the top of the cell. `Middle`: Allign content in the middle of the cell. `Bottom`: Allign content to the bottom of the cell. The default alignment is `middle`.
```json
"_verticalAlignment": "middle",
```

### Fixed colum width 
**Example:** Set's the second column to 200 pixel.
```json
{
    "_column": 1,
    "_width": 200
}
```

## Limitations
No Accessibility support.  

----------------------------
**Author / maintainer:** [DeSimoD](https://github.com/DeSimoD)  
**This is a fork of:** [LearnChamp](https://github.com/LearnChamp)  
**Cross-platform coverage:** Chrome, Chrome for Android, Firefox (ESR + latest version), Edge 12, IE 11, Safari iOS 9+10, Safari OS X 9+10, Opera    
