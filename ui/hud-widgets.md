# HUD Widgets
For your heads-up-display (HUD) - or information you want to show on the screen - you will create UI Widgets.

* Create the widget by right-clicking in the Content Browser (create a UI folder in your project) and choose User Interface > Widget Blueprint.
* In this example we will display the character's speed in a text field on the HUD. Make sure <a href="https://github.com/rickhenderson/developing-in-unreal-engine/blob/main/character-movement-and-setup/README.md">Speed has already been set as a variable in your Animation Blueprint</a>.
* Double-click the widget blueprint to open it.
* In the menu on the left, type in "Canvas" and drag a Canvas Panel into the working area in the centre. This makes it much easier to control where your UI widgets are placed on a variety of screen sizes.
* Next, drag a text block onto the canvas where you want the speed to be displayed. You may have to remove the word "Canvas" from the search bar.

<img src="assets/speed-hud-widget.jpg"/>

* In the image above, I have changed the default text of the speed text box, and added a second textbox to the top of the screen for other debugging.