---
tags: code
hashtags:
- jamstack
- frontend
- webdevelopment
- buildinpublic
---

![[dropdown-menu-without-js.mp4]]

Code snippet with which you will create a simple drop-down menu using only CSS, without JavaScript.

Source: https://codepen.io/LukaszJedrasiak/pen/bGKZoaQ

HTML structure:

```html
<div class="navbar">
	<span id="menu-button">
		<!-- svg path here -->
		
		<!-- menu has to be a child of the button -->
		<span id="menu-content">
			<div class="menu-item"><a href=""><p>Item 1</p></a></div>
			<!-- ...following items -->
		</span>
	</span>
</div>
```


crucial CSS structure:

```css
.navbar {
	height: 72px; // any value, but will be used further
	position: fixed; // or relative
}

#menu-button {
	height: 100%; // button wrapper must fill the entire height of the navbar
}

#menu-content {
	display: none; // invisible by default
	position: absolute; // positioned to the navbar
	top: 72px; // move 72 pixels down starting from the top of the navbar
	left: 0; // move to the left side of the navbar
}

#menu-button:hover #menu-content {
  display: block; // show the menu after hovering the button
}
```
