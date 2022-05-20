## Voeg een personage toe

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
De speler in je wereld zal een kat- of wasbeer-personage zijn. 
</div>
<div>
![de scèneweergave met personage.](images/added-character.png){:width="300px"}
</div>
</div>

--- task ---

Klik op de map **Models** in het Project venster. Een model beschrijft hoe een 3D-object eruit ziet en kan worden gemaakt met 3D-modelleringstools zoals Blender. We hebben enkele modellen toegevoegd die je kunt gebruiken.

Kies het `Cat` of `Raccoon` model en sleep het van het Project venster naar de Scene weergave:

![Animatie van 'Wasbeer' die van het projectvenster naar de scèneweergave wordt gesleept.](images/drag-character.gif)

**Tip:** als je per ongeluk 'CatBase'- of 'RaccoonBase'-modellen hebt toegevoegd, of als je je personage op dit punt wilt wijzigen, kun je het model uit de scène verwijderen. Right-click on the model GameObject in the Hierarchy window and select 'Delete'.

![The Hierarchy window with right-click menu for the model and 'Delete' highlighted.](images/delete-model.png)

--- /task ---

Je personage verschijnt in de scèneweergave in een T-pose.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
De <span style="color: #0faeb0">**T-pose**</span> is de standaardpositie voor een spelpersonage voordat het is geanimeerd.
</p>

--- task ---

Klik op je personage in de scèneweergave en tik op de <kbd>F</kbd> toets.

**Tip:** If you get lost in the Scene view, you can click on your character (or another GameObject) in the Hierarchy window and then click <kbd>Shift</kbd>+<kbd>F</kbd> to focus on your character in the Scene view.

--- /task ---

Hmm, je personage draagt meerdere accessoires.

--- task ---

Click on your character in the Hierarchy window. Hiermee worden de instellingen voor het GameObject geopend in het Inspector venster.

Click on the arrow next to your character in the Hierarchy window to see the 'child objects'. Click on **ConstructionGearMesh** and uncheck the box next to its name in the Inspector window. Dit verbergt de helm en het veiligheidsvest:

![Inspector met de eigenschap 'ConstructieGearMesh' gemarkeerd en uitgeschakeld.](images/uncheck-hat-active.png)

![The Scene view with 'ConstructionGearMesh' removed from the Raccoon.](images/no-hat-scene.png)

Verberg de andere accessoires voor je personage op dezelfde manier, of houd er gewoon een actief.

**Tip:** GameObjects that are not active appear greyed out in the Hierarchy window:

![Hierarchy Window with greyed out 'ConstructionGearMesh'.](images/greyed-out-mesh.png)

--- /task ---

--- task ---

The player will see the game through the 'Main Camera', which is shown as a video camera icon in the Scene. Select the camera in the Hierarchy window to see the embedded camera view:

![Camera geselecteerd in scèneweergave.](images/camera-in-scene.png)

--- /task ---

De spelweergave laat zien hoe je project er voor een speler uit zal zien.

--- task ---

Klik op het Game view tabblad. Je personage bevindt zich in de positie waarnaar je het hebt gesleept in de scèneweergave (je kunt het misschien niet zien).

--- /task ---

Als je genoeg ruimte op je scherm hebt, is het echt handig om de scèneweergave en de spelweergave tegelijkertijd in beeld te hebben.

--- task ---

Sleep het Game view tabblad naar rechts zodat het naast de scèneweergave verschijnt:

![Sleep het Game view tabblad om de spelweergave rechts van de scèneweergave te plaatsen.](images/side-by-side-views.gif)

--- /task ---

Unity gebruikt x-, y- en z-coördinaten om GameObjects in de 3D-ruimte te positioneren:

[[[unity-3D-coordinates]]]

--- task ---

Select your character (in the Hierarchy window or Scene view) and then change its 'Transform' settings so the 'Position' is (0, 0, 0) — the centre of the world:

![Transform for the selected character with position set to 0, 0, 0.](images/transform-centre.png)

Je personage beweegt naar het midden in de scèneweergave en de spelweergave:

![The Scene view with the character at 0, 0, 0 in the middle of the plane.](images/transform-centre-scene-view.png)

--- /task ---

--- task ---

Wijzig de naam van je personage in 'Speler' in het Inspector venster. Dit maakt het makkelijk om meer GameObjects toe te voegen.

![De naam van de speler wordt weergegeven in het venster Inspector.](images/player-name.png)

--- /task ---


--- save ---
