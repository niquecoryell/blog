---
layout: post
title: 'How many clicks do you need to debug ajax request?'
tags: 
- javascript
- debug
- ajax
- efficiency
---


Here I am gonna use Chrome browser as an example:

1. Open context menu
2. Click inspect element.
3. Click "Network" tab
4. Spawn again an ajax request (at least one click. Sometimes more)
5. Click on failed request at Network tab
6. Click "Preview" or "Response" subtab

<!--more-->

<a href="http://i.imm.io/skBN.png">
  <img width="400px" src="http://i.imm.io/skBN.png"/>
</a>

### THIS SHOULD CHANGE

Why we can not automate this daily routine work?

With [this tiny script](https://github.com/bogdan/jquery-ajax-debug) you don't need any:
Error response will be displayed in Popup at once after it occur.

<a href="http://i.imm.io/skDh.png">
  <img width="400px" src="http://i.imm.io/skDh.png"/>
</a>



