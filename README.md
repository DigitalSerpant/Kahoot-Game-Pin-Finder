
# Kahoot Pin Finder Bookmarklet

A JavaScript insert that is used on the offical Kahoot website.


## Authors

- [DigitalSerpant](https://github.com/DigitalSerpant)


## Usage/Examples
Go to [kahoot](https://kahoot.it/) and type "javascript:"
 without the quotes into the search bar of the kahoot tab.
 After you finished typing, paste the following code after
 the text you just typed. Press enter and watch the magic
 happen.
```javascript
(function()%7B document.title = "Close this to stop"%3B document.body.innerHTML = '<div style="display:flex%3Bjustify-content:center%3Balign-items:center%3Bheight:100%%3B"><p style="font-size:3em%3Btext-align:center%3B">Close when done finding pin</p></div>'%3B var interval = setInterval(function() { var code = Math.floor(Math.random() * 9000000 + 1000000)%3B var url = "https://kahoot.it/?pin=" + code + "&refer_method=link"%3B var win = window.open(url, "_blank")%3B setTimeout(function() { if (win.document.querySelector('div[data-functional-selector="notification-bar-error"]')) { win.close()%3B } }, 600)%3B }, 600)%3B %7D)()%3B
```

