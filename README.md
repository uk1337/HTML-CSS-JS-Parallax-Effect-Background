# Parallax Effect Background
This is an example of a parallax effect background using HTML, CSS, and JavaScript. The background image moves slightly in response to the mouse movement, creating a subtle parallax effect.


## Getting Started
To get started with this project, simply clone the repository and open the index.html file in your web browser:

```bash
git clone https://github.com/your-username/parallax-effect-background.git
cd parallax-effect-background
```
Alternatively, you can download the project as a ZIP file and extract it to your desired location.


## Usage
To use this code in your own project, you can copy the relevant HTML, CSS, and JavaScript code into your own files.


### HTML
```html
<div class="background"></div>
<div class="content">
	<h1>Hello, World!</h1>
	<p>This is an example of a parallax effect background.</p>
</div>
```
The HTML code consists of two div elements: one with the background class that contains the background image, and one with the content class that contains the main content of the page.


### CSS
```CSS
body {
	margin: 0;
	padding: 0;
}

.background {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	z-index: -1;
	background: url('background.jpg') no-repeat center center fixed;
	background-size: cover;
}

.content {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	color: white;
	text-align: center;
}
```

The CSS code sets the styles for the body, background, and content elements. The background class has a fixed position and a z-index of -1 to ensure it stays behind the main content. The content class is positioned in the center of the screen using the transform property.


### JavaScript
```js
let background = document.querySelector(".background");

document.addEventListener('mousemove', function (e) {
	let mouseX = event.clientX / window.innerWidth;
	let mouseY = event.clientY / window.innerHeight;
	let movementStrength = 0.125;

	background.style.transform = "translate3d(-" + mouseX * 100 * movementStrength + "px,-" + mouseY * 100 * movementStrength + "px, 0) scale(1.2)";
});
```

The JavaScript code applies the parallax effect to the background element in response to mouse movement. It calculates the mouse position relative to the window size and applies a transform to the background image based on the movement strength and scale.


## License
This project is licensed under the MIT License
