###  Usability: Set individual tab titles

Having multiple tabs open with the same titles makes it hard to find the right tab when you need it, and jumping from tab to tab is hardly a productive activity
This code will set individual tab titles for each tab.

<p align="left">
  <img src="screenshots/setting_tabs_titles.png" >
</p>

☛  Add this JavaScript code in the Header (❓ [Home ► Setup](/common/setup_header.gif)). Click Save and log in again.

```javascript

/**
 * Set individual tab titles
 *
 * @param {string}  [prefix]   - Optional tab prefix
 */
function setTabTitle(prefix) {
    var t = window.nuFORM.getProperty('title');
    if (t === "") {
        t = "Properties";
    }
    prefix = (typeof prefix === "undefined") ? "" : prefix + " - ";
    document.title = prefix + t;
}    

function nuOnLoad() {
    // Set tab titles with the prefix *MyCars* (replace with your nuBuilder instance name)
    setTabTitle("MyCars");   
}
```
