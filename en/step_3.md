## Add a player character

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Add a Cat or Raccoon character.  
</div>
<div>
![The scene view with character.](images/added-character.png){:width="300px"}
</div>
</div>

--- task ---

Double click on the Models folder in the Project Window. A model describes what a 3D object looks like and can be created using 3D modelling tools. We have included some models that you can use. 

Choose either the `Cat` or `Raccoon` model and drag it from the Projects Window to the Scene View.

![Animation of Raccoon being dragged from Project Window to Scene View](images/drag-character.gif)

--- /task ---

Your character will appear in the Scene view. This is the behind-the-scenes view of your game where you set everything up.

--- task ---
Click on your character in the Scene view and tap the 'F' key. 

**Tip:** If you get lost in the Scene view, you can click on your character (or another Game object) in the Hierarchy window and then click 'Shift-F' to focus on your character in the Scene view.

--- /task ---
Hmm, your character is wearing multiple accessories. 

--- task ---
Click on your character in the Hierarchy. This will open the settings for the game object in the Inspector Window.

Click on the arrow next to your Character in the hierarchy to see the ‘child objects’. Click on ‘ConstructionGearMesh’ and uncheck the box next to it’s name in the Inspector. This will hide the hat.

![Inspector with ConstructionGearMesh active property highlighted and unchecked](images/uncheck-hat-active.png)

![The Scene view with ConstructionGearMesh removed from the Raccoon](images/no-hat-scene.png)

Hide the other accessories for your character in the same way, or just keep one active.

**Tip:** Game objects that are not active appeared greyed out in the Hierarchy Window

![Hierarchy Window with greyed out ConstructionGearMesh](images/greyed-out-mesh.png)

--- /task ---

The player will see the game through the Main Camera which is shown as a video camera icon in the scene:

![Camera selected in scene view](images/camera-in-scene.png)

The Game view shows what your project will look like to a Player.

--- task ---
Click on the Game view tab. Your character will be in whatever position you dragged it to in the Scene view (you might not be able to see it). 

--- /task ---

If you have enough room on your screen then it's really useful to see the Scene view and the Game view at the same time. 

--- task ---
Drag the Game view tab to the right so that it appears next to the Scene view:

![Dragging Game view tab to position the Game view to the right of the Scene view](images/side-by-side-views.gif)

--- /task ---

Unity uses X, Y and Z coordinates to position Game objects in 3D space. 

[unity-3d-coordinates]

--- task ---

Select your character (in the Hierarchy or Scene view) and then change its Transform settings so the Position is (0, 0, 0) - the centre of the world.

![Transform for character with position set to 0, 0, 0](images/transform-centre.png)

Your character will move to the centre in the Scene view and the Game view.

![The Scene view with character at 0, 0, 0 in the middle of the plane](images/transform-centre-scene-view.png)

--- /task ---

--- task ---
Rename your character to 'Player' in the Inspector. This will make it easy to find if you add more game objects.

![Player name shown in Inspector.](images/player-name.png)
--- /task ---


--- save ---