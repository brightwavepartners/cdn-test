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
