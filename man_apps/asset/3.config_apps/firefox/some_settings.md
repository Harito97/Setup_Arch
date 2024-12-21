**Here is some setting for Firefox app for better experience**

# To make Firefox bars smaller

Detail in: [How to reduce height of bars in Firefox](https://askubuntu.com/questions/1355169/how-to-reduce-height-of-bars-in-firefox)

```
OPTION ONE:

First, go to about:config in your URL bar.

Then, search for browser.compactmode.show and change the value to true .

Finally, go to the Hamburger-Menu > More-tools > Customize-toolbar and at the bottom of the page, click Density and select Compact.
OPTION TWO:

First, go to about:config in your URL bar.

Then, search for layout.css.devPixelsPerPx

Finally, double click on the value and change it to less than 1.0. After you set the value, press ENTER to apply the changes. For example, you can use 0.75 or if that is too big, you could try 0.5.

NOTE: although the OPTION TWO will affect the whole browser window content like webpages, you can go to about:preferences#general in your URL bar and adjust the "Default zoom" percent to offset the adjusted size
OPTION THREE (probably the best option):

The following solution was originally posted on the Firefox help forums by user cor-el.

    Edit or create the following file using your favorite text editor (nano is used in this example). It should be noted that the file path will be different if you use the Snap version of Firefox!:

nano ~/.mozilla/firefox/*/chrome/userChrome.css

    Add the following lines under the @namespace line (note that the @namespace line is included in the example):

@namespace url("http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul"); /* set default namespace to XUL */


/* ROOT - VARS */
*|*:root {
 --tab-min-height:      25px !important; /* adjust */
 --tab-min-width:       60px !important; /* adjust */
}

/* TABS: height */
#tabbrowser-tabs,
#tabbrowser-tabs > #tabbrowser-arrowscrollbox,
.tabbrowser-tabs .tabbrowser-tab {
  min-height: var(--tab-min-height) !important;
  max-height: var(--tab-min-height) !important;
}

    When you are done editing the file, first make sure Firefox is closed. Then, press CTRL+o to save your file and press CTRL+x to exit nano.

If your user has multiple Firefox profiles saved, nano will automatically open the next profile css file after you press CTRL+x.

And again if you're not using the Snap version of Firefox, and also if that css file doesn't already exist, just allow nano to create the file and then copy and paste the example above (and remember to include the @namespace line if one does not already exist!).

For the Snap version, you will need to find out the default location of your userChrome.css file and then add the contents above as described.

I consider this the best option because it independently reduces the height of the tab bar without scaling other aspects of the browser or web content.
```
