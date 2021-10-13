## Set the 3D scene

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Add a player character and a floor for them to stand on.
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Download the [Unity starter project](http://rpf.io/unity-starter){:target="_blank"} to your computer. 

Unzip/extract the downloaded file on your computer, choose a sensible location such as your Documents folder. 

Launch the Unity Hub and click 'Open' then choose the folder you extracted the downloaded starter project to: 

![The Unity hub with Open Button highlighted](images/unity-hub.png)

Your project will open in the Unity Editor.

--- /task ---

The Unity editor looks like this:

![Unity editor with Windows annotated](images/unity-editor.png)

--- collapse ---

---
title: 1. The Unity Menu
---

The Unity Menu is used to import, open and save scenes and projects. You can amend your Unity Editor preferences and add new Game objects and components. 

--- /collapse ---

--- collapse ---

---
title: 2. The Toolbar
---

The Toolbar contains tools for navigating round in the Scene View, controlling play of the Game View and customising your Unity Editor layout. 

--- /collapse ---

--- collapse ---

---
title: 3. The Scene View
---

The Scene View is used to navigate and edit your Scene. You can select and position Game objects including characters, scenery, cameras and lights.

--- /collapse ---

--- collapse ---

---
title: 4. The Game View
---

The Game View shows the scene as it looks through the lens of your cameras. When you click on the Play button to enter PlayMode The GameView simulates your scene as it would be viewed by a user.  

--- /collapse ---

--- collapse ---

---
title: 5. The Hierarchy Window
---

The Hierarchy View shows all the Game objects in your Scene and the structure between them. You can add and navigate the Game objects in your project. Game objects can had child objects that move with them.

--- /collapse ---

--- collapse ---

---
title: 6. The Project Window
---

The Project Window shows a library of all the files included in your project. You can find Assets to use here.

--- /collapse ---

--- collapse ---

---
title: 7. The Console Window
---

The Console Window shows important messages. This is where you can see Compiler errors (errors in your Script) and messages that you print using Debug.Log().

--- /collapse ---

--- collapse ---

---
title: 8. The Inspector Window
---

The Inspector Window allows you to view and edit the properties of Game objects. You can add other components to your Game objects and edit the values they use. 


--- /collapse ---

--- task ---

The Projects Window is where you can see all the files for your projects including 'Assets' that you can use in your project.

Click on the Projects tab and make sure you can see the Assets included in the starter project:

![Project View selected with folders shown](images/project-view-folders.png)

--- /task ---

In Unity, a Scene contains Game objects. A game with multiple levels might have one scene per level. 

--- task ---

Click 'File -> Save As' and name your Scene '3D World'. 

Select the location dropdown and navigate to your `Scenes` folder:

![The save as popup window with Scenes folder selected](images/save-scene.png)

A new file will appear in the Project Window:

![Projects Window with 3D World scene in the Scenes folder](images/3dworld-scene.png)

--- /task ---

--- task ---

Double click on the Models folder. A model describes what a 3D object looks like and can be created using 3D modelling tools. We have included some models that you can use. 

Choose either the `Cat` or `Raccoon model` and drag it from the Projects Window to the Scene View.

![Animation of Raccoon being dragged from Project Window to Scene View](images/drag-character.gif)

--- /task ---

Your character will appear in the Scene view. This is the behind-the-scenes view of your game where you set everything up.

--- task ---
Click on your character in the Scene view and tap the 'F' key. This will focus on your character. You can also use the scroll wheel on your mouse to zoom in and out. 

**Tip:** If you get lost in the Scene view, you can click on your character (or another game object) in the Hierarchy window and then click 'Shift-F' to focus on your character in the Scene view.

--- /task ---

Hmm, your character is wearing multiple accessories. 

--- task ---

Click on your character in the Hierarchy. This will open the settings for the game object in the Inspector Window.

Click on the arrow next to your Character in the hierarchy to see the 'child objects'. Click on 'ConstructionGearMesh' and uncheck the box next to it's name in the Inspector. This will hide the hat. 

![Inspector with ConstructionGearMesh active property highlighted and unchecked](images/uncheck-hat-active.png)

Hide the other accessories for your character in the same way, or just keep one active. 

**Tip:** Game objects that are not active appeared greyed out in the Hierarchy Window

![Hierarchy Window with greyed out ConstructionGearMesh](images/greyed-out-mesh.png)

--- /task ---

Your character is floating in the air! 

--- task ---

Right-click on your scene (name '3D World') in the Hierachy and choose 'GameObject' -> '3D Object' -> 'Plane'. 

![The 3D World scene with menu extended and plane highlighted](images/add-plane.png)

This will create a 'Floor' for your World. 

The default size for the plane is 10m x 10m. Unity uses metres as the unit of measurement. 

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

![Dragging Game view tab to position the Game view to the right of the Scene view](images/side-by-side-views.png)

--- /task ---

Unity uses X, Y and Z coordinates to position Game objects in 3D space. 

[unity-3d-coordinates]

--- task ---

Click on your character in the Hierarchy and then change its Transform settings so the Position is (0, 0, 0) - the centre of the world.

![Transform for character with position set to 0, 0, 0](images/transform-centre.png)

Your character will move to the centre in the Scene view and the Game view.

--- /task ---

--- save ---