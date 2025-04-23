# aps-viewer-multiselection
Sample to control Viewer multi-selection

## How it works

This sample overrides the current Viewer mechanism for selecting elements through an Extension that leverages a custom Tool.

Every time a user clicks in the Viewer, it triggers the `handleSingleClick` function.
This function basically verifies if the CTRL key is selected, and if so, it aggregates the current element selected to select multiple elements.
When the CTRL key is released then it goes back to the default behavior.

## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT). Please see the [LICENSE](LICENSE) file for full details.

## Written by

João Martins [in/jpornelas](https://linkedin.com/in/jpornelas)