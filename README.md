# Bookmarklets for Gmail Basic HTML version :email: :dash:

I prefer the [basic version](https://mail.google.com/?ui=html) because it's way simpler but perhaps _too simple_, so let me introduce these bookmarklets are in order to have a better ux.  
Just in case you're wondering wtf are they:

> Bookmarklets are unobtrusive JavaScripts stored as the URL of a bookmark in a web browser or as a hyperlink on a web page.

(Source: [Bookmarklet Wikipedia page](https://en.wikipedia.org/wiki/Bookmarklet))

Note: There's an [Github Markup - open issue](https://github.com/github/markup/issues/79) to allow creating `javascript:` links on `README`s, meanwhile you can either go to the [webpage version of this document](https://cyberpunk.com.ar/gmail-basic-html-bookmarklets/) or scroll down to know [how it's done in your browser](https://cyberpunk.com.ar/gmail-basic-html-bookmarklets/#how-do-i)).

### Inbox

Performs a search using `in:inbox is:unread` filter.  

[📥 Inbox](javascript:(function(){document.querySelector("#sbq").value = "in:inbox is:unread";document.querySelector("input[name='nvp_site_mail']").click();}());)

```javascript
javascript: (function() {
  document.querySelector("#sbq").value = "in:inbox is:unread";
  document.querySelector("input[name='nvp_site_mail']").click();
}());
``` 

### Unread

Performs a search using _whatever is in your search box_ + `is:unread` filter.  

[📩 Unread](javascript:(function(){var sbq=document.querySelector("#sbq");sbq.value=sbq.value+" is:unread";document.querySelector("input[name='nvp_site_mail']").click();}());)

```javascript
javascript: (function() {
  var sbq = document.querySelector("#sbq");
  sbq.value = sbq.value +" is:unread";
  document.querySelector("input[name='nvp_site_mail']").click();
}());
``` 

### Select all

Will check _every_ checkbox in the current result page.

[📕 Select All](javascript:(function(){var inp=document.querySelectorAll("tr > td > input");for(var i=0;i<inp.length;i++){inp[i].checked=true;}}());)

```javascript
javascript: (function() {
  var inp = document.querySelectorAll("tr > td > input");
  for (var i = 0; i < inp.length; i++){ inp[i].checked = true; }
}());
``` 

### Select unread

Will check only those with _white background_ (ie: unread) checkbox in the current result page.

[📗 Select Unread](javascript:(function(){var inp=document.querySelectorAll("tr[bgcolor='#ffffff'] > td > input");for(var i=0;i<inp.length;i++){inp[i].checked=true;}}());)

```javascript
javascript: (function() {
  var inp = document.querySelectorAll("tr[bgcolor='#ffffff'] > td > input");
  for (var i = 0; i < inp.length; i++){ inp[i].checked = true; }
}());
``` 

## Q & A?

### These are not working! 

I use (and recommend) Firefox and haven't tried on other browsers, so please [report it](https://github.com/lvm/gmail-basic-html-bookmarklets/issues) if you found an issue.

### How can I add a bookmarklet?

That'll depend on your browser.

* [Mozilla Firefox](https://support.mozilla.org/en-US/kb/bookmarklets-perform-common-web-page-tasks)
* [Google Chrome](https://support.google.com/chrome/answer/188842?co=GENIE.Platform%3DDesktop&hl=en)
* [Apple Safari](https://support.apple.com/guide/safari/bookmark-webpages-that-you-want-to-revisit-ibrw1039/mac)


## LICENSE

See [LICENSE](LICENSE)
