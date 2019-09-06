---
layout: post
title: iPhone-like password fields using jQuery
description:
author: su
featured: true
---

**or: Delayed password masking with JavaScript.**

==This lib is deprecated. Sorry.==

Jakob Nielsen recently asked us to [Stop Password Masking](http://www.useit.com/alertbox/passwords.html):

> Usability suffers when users type in passwords and the only feedback they get is a row of bullets. Typically, masking passwords doesn’t even increase security, but it does cost you business due to login failures.  
> <small>[useit.com/alertbox/passwords.html](http://www.useit.com/alertbox/passwords.html)</small>

He suggests using **plain text input fields by default** and offering a **checkbox** to have the passwords masked.

We do not completely go for the idea of typing passwords in plain text by default as there *will* be a loss of security! Not a technical one, but a user-driven one.

---

### Password fields on iPhone/iPod touch

![iphone-password](/content/images/2015/02/iphone-password.jpg)

Of course Nielsen is right when he talks about users making more errors and feeling less confident when they can’t see what they’re typing while filling in forms. That may have been the reason why Apple <del>developed</del> implemented an alternative method on **iPhone/iPod Touch**: passwords get masked while typing but the last character in row is shown in plain text. Compared to common password fields on the web this method improves usability, not only on mobile devices. And concerning security risks you’ll probably need James Bond behind your back looking over your shoulders in order to let your password be captured.

So, this method looks to be a pretty good way of typing in passwords, and that is why tried to use it on web forms. It comes as a **jQuery plugin** which works unobtrusive. Non-JS users get the common masked password fields.

Copy & paste will work as usual. The only thing that will not work is: deleting/inserting single or multiple characters from the beginning/middle of the masked password string.  
 But, let’s face it, who will do that?

## Live demo

_(Disabled, sorry.)_

### Features

1. Doesn’t need any HTML modification as it finds password fields by type.
2. Unobtrusive: Non-JS users get the common masked password fields.
3. Supports copy & paste.
4. Options: Interval, delay, replacement character, prefix, debug mode.

### Instructions

It’s very simple.

1. Just load jQuery, of course ;-).
2. Load the Plugin
3. and then initialize dPassword.

You are done!

```
<script src="/js/jquery.js" type="text/javascript"></script><script src="/js/jQuery.dPassword.js" type="text/javascript"></script><script type="text/javascript">
  $(document).ready( function() {
    $('input:password').dPassword();
  });
</script>
```

There are some options you might want to configure:

- **interval**  
Time in msec the scripts checks for newly entered characters.
- **duration**  
Delay in msec of converting the last entered character.
- **replacement**  
The character to be replaced, for unicode characters use the following format: `%u25CF`  
You may check these ressources: [Overview of unicode characters](http://www.utf8-chartable.de) or a more comprehensive [overview](http://www.fileformat.info/format/w3c/entitytest.htm?sort=Unicode+Character).
- **prefix**  
This is the prefix of the newsly generated elements. Default is `password_`.
- **debug**  
For debugging issues. You need FireBug enabled!

Example:

```
<script src="/js/jquery.js" type="text/javascript"></script><script src="/js/jQuery.dPassword.js" type="text/javascript"></script><script type="text/javascript">
  $(document).ready( function() {
    $('input:password').dPassword({
      duration: 2000,
      prefix: 'my_'
    });
  });
</script>
```

### Known Issues

1. Adding/deleting chars from the middle doesn’t work. Works at the end of the password only.
2. View will not follow cursor if input field is too small.
3. If #id based CSS styles are assigned, these styles will not be taken over.

### Download

**Project page with SVN repository: [http://code.google.com/p/dpassword/](http://code.google.com/p/dpassword/)**  

JS download: [jQuery.dPassword.js](http://dpassword.googlecode.com/svn/trunk/lib/jQuery.dPassword.js)  
 Complete ZIP download: [dpassword.zip](http://dpassword.googlecode.com/files/dpassword.zip)
