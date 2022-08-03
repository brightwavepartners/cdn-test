# What is it?

Very simply, a quick HTML page that will load some Javascript code. The idea for the page is to be able to load the Javascript code from a CDN source to verify  that the CDN is functioning properly.

## Usage

The index.htm file loads some Javascript code that displays the date and time when a button is clicked.

```html
<!-- load script locally first to make sure things are working,
     then swap the local script location with a cdn location to
     check that it still works and inspect headers to verify. -->
<script src="datetime.js"></script>
```

The `<script>` line loads the Javascript code and is currently set to load from a local file. Switch the `src` location to a CDN to load the Javascript from the CDN.

To verify CDN functionality, open the index.htm file in a browser and click on the **Click me to display Date and Timne** button. If the Javascript has been successfully loaded from the CDN, a message box should popup with the current date and time.

Additionally, you can check correct CDN functionality by inspecting the headers on the datetime.js Javascript file that is loaded into the browser. Open the developer tools of the browser (usually by pressing F12) and take a look at the headers. Verify the **Request URL** is the CDN location. If the CDN source has cache-control set, verify that the **cache-control** header is present and is correct. Finally, the **x-cache** header should indicate a HIT. It may take a second reload of the page for the cache to register a HIT.