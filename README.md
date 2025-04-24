# aps-viewer-multiselection
Sample to control Viewer multi-selection

## How it works

This sample overrides the current Viewer mechanism for selecting elements through an Extension that leverages a custom Tool.

Every time a user clicks in the Viewer, it triggers the `handleSingleClick` function.
This function basically verifies if the CTRL key is selected, and if so, it aggregates the current element selected to select multiple elements.
When the CTRL key is released then it goes back to the default behavior.

## Other option

You can also leverage the BoxSelection extension to retrieve all the elements in the view using the snippet below

```
async function getViewElements(viewer){
  const tool = viewer.getExtension('Autodesk.BoxSelection').boxSelectionTool;
  const {left: startX, top: startY, right: endX, bottom: endY} = viewer.impl.getCanvasBoundingClientRect();
  tool.startPoint.set(startX, startY);
  tool.endPoint.set(endX, endY);
  let selection = await tool.getSelection();
  console.log(selection);
}
```

## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT). Please see the [LICENSE](LICENSE) file for full details.

## Written by

João Martins [in/jpornelas](https://linkedin.com/in/jpornelas)
