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

**Tip:** als je per ongeluk 'CatBase'- of 'RaccoonBase'-modellen hebt toegevoegd, of als je je personage op dit punt wilt wijzigen, kun je het model uit de scène verwijderen. Klik met de rechtermuisknop op het model GameObject in het venster hiërarchie en selecteer 'Delete'.

![Het venster Hierarchy met het snelmenu voor het model en 'Delete' gemarkeerd.](images/delete-model.png)

--- /task ---

Je personage verschijnt in de scèneweergave in een T-pose.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
De <span style="color: #0faeb0">**T-pose**</span> is de standaardpositie voor een spelpersonage voordat het is geanimeerd.
</p>

--- task ---

Klik op je personage in de scèneweergave en tik op de <kbd>F</kbd> toets.

**Tip:** als je verdwaald raakt in de scèneweergave, kun je in het Hierarchy venster op je personage (of een ander GameObject) klikken en vervolgens op <kbd>Shift</kbd>+<kbd>F</kbd> klikken om te centreren op je personage in de scèneweergave.

--- /task ---

Hmm, je personage draagt meerdere accessoires.

--- task ---

Klik op je personage in het venster Hierarchy. Hiermee worden de instellingen voor het GameObject geopend in het Inspector venster.

Klik op de pijl naast je personage in het Hierarchy venster om de 'onderliggende objecten' te bekijken. Klik op **ConstructieGearMesh** en schakel het selectievakje naast de naam uit in het venster Inspector. Dit verbergt de helm en het veiligheidsvest:

![Inspector met de eigenschap 'ConstructieGearMesh' gemarkeerd en uitgeschakeld.](images/uncheck-hat-active.png)

![De Scèneweergave met 'ConstructieGearMesh' verwijderd uit de Wasbeer (Raccoon).](images/no-hat-scene.png)

Verberg de andere accessoires voor je personage op dezelfde manier, of houd er gewoon een actief.

**Tip:** Gameobjecten die niet actief zijn, worden grijs weergegeven in het venster Hierarchy:

![Hierarchy venster met 'ConstructieGearMesh' grijs weergegeven.](images/greyed-out-mesh.png)

--- /task ---

--- task ---

De speler ziet het spel via de 'Main Camera', die in de scène wordt weergegeven als een videocamera-pictogram. Selecteer de camera in het venster Hierarchy om de ingesloten cameraweergave te bekijken:

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

Selecteer je personage (in het venster Hierarchy of de scèneweergave) en wijzig vervolgens de 'Transform'-instellingen zodat de 'positie' (0, 0, 0) is — het centrum van de wereld:

![Transformatie voor het geselecteerde personage met positie ingesteld op 0, 0, 0.](images/transform-centre.png)

Je personage beweegt naar het midden in de scèneweergave en de spelweergave:

![De scèneweergave met het personage op 0, 0, 0 in het midden van het vlak.](images/transform-centre-scene-view.png)

--- /task ---

--- task ---

Wijzig de naam van je personage in 'Speler' in het Inspector venster. Dit maakt het makkelijk om meer GameObjects toe te voegen.

![De naam van de speler wordt weergegeven in het venster Inspector.](images/player-name.png)

--- /task ---


--- save ---
