## Set the 3D scene

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Your 3D world,  or 'map', needs a floor and walls. 
</div>
<div>
![The scene view showing a plane floor with two brick walls.](images/end-walls.png){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
People are spending more time in <span style="color: #0faeb0">**online virtual environments**</span>. As well as playing games, people relax, explore, socialise, learn, and participate in interactive entertainment. Some people call the future of these environments the <span style="color: #0faeb0">**metaverse**</span>. Being able to design 3D worlds is an important skill.
</p>

A Unity project needs graphics and sound 'Assets'.  

--- task ---

Download the [Unity starter package](https://rpf.io/p/en/explore-a-3d-world-go){:target="_blank"} to your computer. Choose a sensible location such as your Documents folder. 

--- /task ---

--- task ---

Launch the Unity Hub and click **Projects** then select **New project**:

![The 'New project' button on the top right of the unity hub.](images/new-project.png)

From the list of templates, select **3D Core**: 

![A list of templates. The one called '3D' is selected; it has a subheading of 'Core' underneath.](images/3D-core.png)

Edit the Project Settings to give your project a sensible name and save it to a sensible location. Then click **Create project**:

![The project's settings area with 'Create project' button highlighted in the bottom right corner.](images/create-project.png)

Your new project will open in the Unity Editor.

--- /task ---

The Unity Editor looks like this:

![Unity Editor with Windows annotated.](images/unity-editor.png)

--- collapse ---

---
title: The Unity Editor windows and views
---

1. **The Unity Menu** is used to import, open, and save scenes and projects. You can amend your Unity Editor preferences and add new GameObjects and components. 

2. **The Toolbar** contains tools for navigating round in the Scene View, controlling play in the Game View, and customising your Unity Editor layout. 

3. **The Scene View** is used to navigate and edit your Scene. You can select and position GameObjects including characters, scenery, cameras, and lights.

4. **The Game View** can be accessed by clicking on the **Game** tab. It shows the scene as it looks through the lens of your cameras. When you click on the **Play** button to enter Playmode, the Game View simulates your scene as it would be viewed by a user. 

5. **The Hierarchy Window** shows all the GameObjects in your Scene and the structure between them. You can add and navigate the GameObjects in your project. GameObjects can have 'child objects' that move with them.

6. **The Project Window** shows a library of all the files included in your project. You can find the Assets you want to use here.

7. **The Console Window** can be accessed by clicking on the **Console** tab. It shows important messages. This is where you can see Compiler errors (errors in your Script) and messages that you print using `Debug.Log()`.

8. **The Inspector Window** allows you to view and edit the properties of GameObjects. You can add other components to your GameObjects and edit the values they use. 

--- /collapse ---

--- task ---

The 'Unity starter package' you downloaded contains a number of Assets for you to use in your project. 

To import them into your new project, click on the **Assets** menu and select **Import package** > **Custom Package...** then navigate to the downloaded 'Unity starter package'.

--- /task ---

[[[unity-importing-a-package]]]

--- task ---

The **Project Window** is where you can see all the files included in your project. Click on the **Models** folder in the Assets option to see the models you have imported.

![Project View selected with folders shown.](images/project-view-folders.png)

--- /task ---

In Unity, a **Scene** contains GameObjects. A Unity project with multiple game levels might have one scene per level. 

--- task ---

Right-click on **SampleScene** in the Hierarchy and choose **Save Scene As**. 

![The scene icon in the Hierarchy window with the right-click menu expanded.](images/right-click-scene.png)

In the popup window, name your Scene '3D World':

![The 'Save As' popup window with Scenes folder selected.](images/save-scene.png)

A new file will appear in the Project Window:

![Projects Window with 3D World scene in the Assets folder.](images/3dworld-scene.png)

--- /task ---

Your world needs some ground. 

--- task ---

Right-click on your scene (name '3D World') in the Hierarchy and choose **GameObject** > **3D Object** > **Plane**: 

![The 3D World scene with menu extended and 'Plane' highlighted.](images/add-plane.png)

This will create a 'Ground' for your World. 

The default size for the plane is 10m × 10m. Unity uses metres as the unit of measurement. 

![The Scene view with a large white plane.](images/plane-floor.png)

--- /task ---

The **material** of a GameObject controls how it looks. Give the plane a different colour material.

--- task ---

In the Project Window, right-click on the **Materials** folder and choose **Create** > **Material**.

![The 'Create' menu showing 'Material' highlighted.](images/create-material.png)

A new material should appear. Decide what colour you will use for your floor and name your new material:

![Icon for a new material with the name highlighted.](images/new_material.png)

Click on the colour next to 'Albedo' in the Inspector Window and choose a colour for your material (we used grey):

![The colour bar to the right of 'Albedo' is filled in grey.](images/grey-plane-material.png)

Drag your new material from the Project Window to your plane in the Scene View:

![The grey material in the Project Window.](images/grey-material.png)

![The Scene View with a grey plane.](images/gray_plane.png)

--- /task ---

You can create objects from 3D shapes. 

--- task ---

Right-click on your '3D World' scene in the Hierarchy window and choose 'GameObject' -> '3D Object' -> 'Cube'. 

This will create a cube at the centre of the scene, at (0, 0, 0).

![small cube in centre of the plane](images/new_cube.png)

--- /task ---

You can see the cube in the Scene view. This is the behind-the-scenes view of your game where you set everything up.

**Tip:** Click on the 'Scene' tab to make sure you can see the Scene view. 

--- task ---

Click on the Cube in the Scene view or Hierarchy window to select it.

Use 'Shift-F' (hold down the Shift key and tap F) to focus on the cube. 

You can also use the scroll wheel on the mouse, or the up and down arrow keys, to zoom in and out:

![The cube in the centre of the scene view half above and half below the plane.](images/cube-scene-view.png)

--- /task ---

You need to get the cube to sit on the plane. 

--- task ---

Click on the Cube in the Scene view or Hierarchy window to select it.

**Choose** You can either:

+ Change the Y position in the Inspector to 0.5 (half the height of the cube):

![The Transform component for the Cube with the y position coordinate set to 0.5](images/y-transform-cube.png)

+ Drag the green arrow up until the cube sits on the plane:


![An animated gif showing the move arrows on the cube with the mouse pointer dragging up the y axis so the cube rises and sits on the plane.](images/drag-y-axis.gif)

--- /task ---

**Tip:** If you make a mistake in the Unity editor you can use 'Ctrl-Z' ('Cmd-Z') to **undo** your last action. 

--- task ---

Now change the cube into a wall with the following Position and Scale settings: 

![The transform component with updated position and scale properies, Position X=0, Y=1, Z=3, Scale X=5, Y=2, Z=0.25.](images/transform-cube-to-wall.png)

You can either enter the values in the Transform for the Cube or drag the arrows (this will update the Transform values.)

Zoom out to see your wall:

![The new positioned and scaled wall in the scene view.](images/scene-cube-wall.png)

--- /task ---

A material can have a colour and a texture and there are lots of properties that you can adjust to get different effects. A **texture** is a 2D image that can be created in an image editor.

--- task ---

In the Project window, right-click on the ‘Materials’ folder and choose ‘Create’ -> ‘Material’. You are going to create a coloured brick wall. Give the material a descriptive name:

![The 'Create' menu showing 'Material' highlighted.](images/create-material.png)

Click on the colour next to ‘Albedo’ in the Inspector window and choose a colour for your material:

![The coloured bar to the right of 'Albedo' is filled in red.](images/red-colour.png)

Add a texture by clicking on the circle to the left of ‘Albedo’ and selecting 'BrickWallAlbedo' texture from the list: 

![The popup window to select a texture with 'BrickWallAlbedo' highlighed.](images/add-texture.png)

Drag your new material from the Project window to your wall in the Scene view:

![The red brick material in the Project window.](images/brick-material.png)

![The scene view with red brick wall.](images/red-brick-wall.png)

--- /task ---

--- task ---

In the Inspector window, right click on your cube, choose 'Rename' from the menu and rename your object from 'Cube' to `Wall`:

![Inspector showing Wall as the name.](images/name-wall.png)

**Tip:** You can name a new GameObject in the Hierarchy window when you create it and you can change the name in the Inspector window.

--- /task ---

--- task ---

To create a copy of your wall you can either:
+ Right-click on your 'Wall' object in the Hierarchy window and choose 'Duplicate'. 
+ Select your wall in the Scene view and use 'Ctrl-D' (or 'Cmd-D') to duplicate.

Your new wall will be in exactly the same place as your first wall. 

--- /task ---

--- task ---

Change the Y rotation of the new wall to `90`: 

![The new wall transform component with rotate on the y axis showing 90 degrees ](images/transform-rotate-90.png)

--- /task ---

--- task ---

Reposition the new wall to following position:

![Transform for new wall. Position X=4, Y=1, Z=-1.](images/new-wall-transform.png)

You can either enter the values in the Inspector window or drag the arrows in the scene - it doesn't matter if the position is exact.

Your scene should look like this:

![Scene with two red brick walls.](images/scene-with-walls.png)

--- /task ---

--- task ---

Click on your Plane. Change the 'Scale' settings on the Plane to make it bigger so you have more room: 

![The transform component with scale X and Z coordinates changed to 4](images/plane-scale-4-1-4.png)

![The Scene view showing the larger plane](images/new-resized-plane.png)

Think of a 4x4 plane as 40 metres by 40 metres in the real world. Plenty of room for your character to move around.

--- /task ---

--- task ---

When you have unsaved changes you will see a '*' next to your scene in the Hierarchy window.

Save your scene by clicking 'File' -> 'Save' or 'Ctrl-S'. 

Also, save your project by clicking 'File' -> 'Save Project'.

Unity does not normally autosave changes, but your starter project contains a script to autosave your project every 60 seconds. 

--- /task ---

You can navigate around your scene to see it from different angles. If you get lost just click on a wall in the Hierarchy window and then 'Shift-F' to focus and then zoom out: 

[[[unity-scene-navigation]]]

Remember, if you navigate around then you will be looking at your scene from a different perspective so your view won't look exactly the same as our examples.

--- save ---
