---
layout: post
title: Mark external links and open in new window/tab (jQuery)
description: "A jQuery snippet to parse external links and open them in new windows/tabs on click."
author: ds
more: true
---

**Specs:**

1. filter external links (check the hostname)
2. filter links marked as `rel="external"`
3. filter links in image maps (`area`) as well
4. text links only (do not contain `img`, `div` or `mailto`): add CSS class `.external` providing an additional icon
5. open external links in new window/tab

**The code (jQuery):**

```
$(document).ready(function(){
  $('a, area').filter(function() {
    return this.hostname && (this.hostname).split(":")[0]
      !== (location.hostname).split(":")[0]
    || $(this).attr('rel') == 'external';
  })
  .not(':has(img, div, mailto)')
  .addClass('external')
  .end()
  .click(function(e) {
    open(this.href); 
    e.preventDefault();
  });
});
```

**Notes:**

- Why not mark external links containing `images`, `div` or `mailto` with CSS class `.external`? This is because we want to add the icon to pure text links only. Links containing images or whatever kind of block elements may disturb the site layout if an additional icon would be added.
- Use `rel="external"` to force opening a link in a new window/tab.

**CSS providing an icon for external links marked with class .external:**

```
a.external {
  background-image: url(icon_external.png);
  background-position: right top;
  background-repeat: no-repeat;
  padding-right: 11px;
  zoom: 1; /* IE */
}
```

(Inspired by [Karl Swedberg at learningjquery.com](http://www.learningjquery.com/2008/08/quick-tip-dynamically-add-an-icon-for-external-links).)


