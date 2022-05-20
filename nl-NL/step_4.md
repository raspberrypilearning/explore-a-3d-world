## Voeg een beweging toe

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Je speler beweegt met de WASD- of pijltjestoetsen. 
</div>
<div>
![de scène in Spelweergave met personage dat door de scène beweegt.](images/moving-character.gif){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Unity werkt met de <span style="color: #0faeb0">**C#**</span> (uitgesproken als C Sharp) programmeertaal, die wordt gebruikt door professionele software-ontwikkelaars. C# is een object-georiënteerde taal met **classes** die gedrag voor vergelijkbare objecten definiëren en met **methods**, wat functies zijn die tot een class behoren. In Unity definieert een **script** een class met variabelen en methods. Je kunt hetzelfde script aan meerdere GameObjects toevoegen als ze dezelfde functies nodig hebben.</p>

--- task ---

Click on the **Player** GameObject in the Hierarchy window or Scene view so you can see its properties in the Inspector window.

![Het Player Game Object geselecteerd in de hiërarchie.](images/player-selected.png){:width="300px"}

**Tip:** Make sure you have the **Player** selected and not one of its child objects.

Klik op **Add Component** en typ `character` in het zoekvak en klik vervolgens op de **Character Controller** component wanneer deze verschijnt:

![Het menu 'Add Component' met de character controller.](images/character-controller-add.png)

--- /task ---

The Character Controller component adds new features to your Player GameObject including a `SimpleMove` method and a **collider**. Colliders kunnen worden gebruikt om te zorgen dat je personage niet door vaste voorwerpen loopt en om te detecteren wanneer botsingen plaatsvinden.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
 Een <span style="color: #0faeb0">**collider**</span> is een vorm die wordt gebruikt om te detecteren wanneer een GameObject botst of kruist met een ander GameObject. De computer kan veel sneller controleren op botsingen met een eenvoudige botsvorm dan met de complexe vorm van een GameObject. Een **hitbox** is een soort botsing. </p>

--- task ---

De Character Controller Collider heeft een hoogte van `2` en een middelpunt op `0, 0, 0`; dit betekent dat deze half boven en half onder het vlak is geplaatst:

![De scèneweergave toont het personage met een Character Controller-capsule rond het model.](images/scene-char-controller.png){:width="300px"}

Your character has a height of `1`, meaning their centre on the y-axis is at `0.5`. Wijzig de waarde in het centrum van de y-as van de Character Controller in `0.5` en de hoogte in `1` om het aan te passen aan je personage:

![De eigenschappen van het Inspector venster van de Character Controller component.](images/properties-controller.png){:width="400px"}

![De scèneweergave toont het personage met een Character Controller capsule rond het model.](images/updated-char-controller.png){:width="300px"}

--- /task ---

Je personage heeft een script nodig zodat de speler het kan verplaatsen. Je hebt een code-editor nodig die op je computer is geïnstalleerd om dit script te kunnen bewerken.

[[[unity-visual-studio]]]

--- task ---

Go to the Inspector window for the Player and click on the **Add Component** button. Typ `script` en selecteer **New Script**. Geef je nieuwe script een naam `PlayerController` en druk vervolgens op <kbd>Enter</kbd>.

Het nieuwe script wordt opgeslagen in de map Assets:

![Het Project venster met de nieuwe 'My Scripts' map wordt weergegeven.](images/new-script-project.png){:width="400px"}

--- /task ---

--- task ---

Dubbelklik op **PlayerController** in het script-onderdeel in het Inspector-venster. Het script wordt geopend in een aparte code-editor en heeft deze code:

--- code ---
---
language: cs filename: PlayerController.cs line_numbers: true line_number_start:
line_highlights:
---
using System.Collections; using System.Collections.Generic; using UnityEngine;

public class PlayerController : MonoBehaviour
{ // Start is called before the first frame update void Start()
    {

    }
    
    // Update is called once per frame
    void Update()
    {
    
    }
} --- /code ---

**Debug:** Controleer of de naam na 'class' `PlayerController` is en dit overeenkomt met de naam van je scriptbestand: Als je het bestand een andere naam geeft nadat je het hebt gemaakt, moet je de class name in het script wijzigen.

--- /task ---

De Start methode wordt eenmaal aangeroepen wanneer je de scène afspeelt. Add code to print the message `Player started` when your project starts running.

--- task ---

Gebruik de `Debug.Log()` methode om een bericht te tonen wanneer de `Start` methode wordt aangeroepen voor het Player Gameobject. Het bericht verschijnt in de balk onder aan de Unity Editor en in het Console-venster:

--- code ---
---
language: cs filename: PlayerController.cs - Start() line_numbers: true line_number_start: 7
line_highlights: 10
---

    // Start is called before the first frame update
    void Start()
    {
        Debug.Log("Player started");        
    }
--- /code ---

**Tip:** de regels die beginnen met // zijn opmerkingen die de code toelichten. Je hoeft ze niet te typen.

**Sla het PlayerController script op** met <kbd>Ctrl</kbd>+<kbd>S</kbd> (of <kbd>Cmd</kbd>+<kbd>S</kbd>) en keer vervolgens terug naar de Unity Editor. De Unity Editor zal je script laden om het klaar te maken voor gebruik; dit kan een paar seconden duren.

--- /task ---

--- task ---

Klik op het tabblad van het consolevenster om het naar voren te brengen:

![Het tabblad voor het Console venster dat linksonder in de Unity Editor is gemarkeerd.](images/console-window.png){:width="400px"}

--- /task ---

--- task ---

**Test:** Ga naar de werkbalk en klik eenmaal op de knop **Play** om de scène in de afspeelmodus te zetten. Dit zal je scène simuleren zoals het zou worden bekeken en interactief toegepast door een gebruiker:

![De werkbalk bovenaan de Unity Editor met de knop Play gemarkeerd.](images/play-button.png){:width="400px"}

Unity takes a few seconds to start up, then you should see the `Debug.Log()` 'Player started' output in the Console.

![The Console window with the time-stamped 'Player started' message as a comment.](images/player-started.png)

**Debug:** je scène wordt niet afgespeeld als er fouten in je code zijn. Controleer het Console-venster voor informatie. You may see:
+ `; expected` – check for a semicolon `;` at the end of each line of code.
+ `Newline in constant` – you missed a quote `"` from the end of a text string.
+ `} expected` – you should have a pair of open and close curly brackets `{}` around each method and around the class. Check that your curly brackets match.
+ `) expected` – make sure there's a closing `)` at the end of each method call, before the semicolon.
+ `Debug` does not contain a definition for 'log' – C# is case sensitive, so it needs to be `Log` with a capital `L`.

Compare your code with the example code and make sure everything is exactly the same.

--- /task ---

--- task ---

Click once on the **Play** button again to exit Play mode and the debug output will stop.

**Tip:** Changes made in Play mode are lost when you exit Play mode. Make sure you exit Play mode when you finish testing.

--- /task ---

Unity creates the effect of movement by quickly drawing images to the screen. Each image is a **frame**. The `Update` method is called once every frame.

--- task ---

You will be able to use the WASD or arrow keys (players on a mobile or console can use different inputs without you changing your code.)

`Input.GetAxis("Vertical")` takes input from the <kbd>W</kbd> and <kbd>S</kbd> keys or the up and down arrow keys, and returns a number between 1 and -1, which it uses for forwards and backwards movement.

--- code ---
---
language: cs filename: PlayerController.cs - Update() line_numbers: true line_number_start: 14
line_highlights: 16-21
---

    void Update()
    {
        float speed = Input.GetAxis("Vertical");
    
        if (speed != 0) // Player moving
        {
            Debug.Log(speed);
        }
    }
--- /code ---

A `float` is a decimal number.

**Save** your PlayerController script in your code editor, using <kbd>Ctrl</kbd>+<kbd>S</kbd> (or <kbd>Cmd</kbd>+<kbd>S</kbd>), then return to the Unity Editor.

**Tip:** You might finding it quicker to use <kbd>Alt</kbd>+<kbd>Tab</kbd> (or <kbd>Cmd</kbd>+<kbd>Tab</kbd>) to switch between your web browser with the project instructions, the Unity Editor, and your code editor.

--- /task ---

--- task ---

**Test:** Go to the Toolbar and click on the **Play** button to put your scene into Play mode.

Place your **mouse pointer in the Game view** and press keys <kbd>W</kbd> and <kbd>S</kbd>. Look at the values logged in the Console window as you press the keys. Each time you press <kbd>W</kbd> a positive number is logged, when you press <kbd>S</kbd> a negative number is logged.

The numbers range between -1.0 and 1.0 and correspond to movement from the vertical controls on the keyboard (or a game controller). You can also use the up and down arrow keys.

![The Console window with five log entries that have values between -1 and 1.](images/console-values.png)

**Tip:** The output also appears in the bar at the bottom of the Unity Editor.

Click the **Play** button again to exit Play mode and the debug output will stop.

--- /task ---

It's easy to forget whether your game is playing or not. A Play mode colour tint makes it easier to tell when your scene is playing:

![Side-by-side images of the Unity Editor without tint and with tint to indicate the game is playing.](images/tint-no-tint.png)

--- task ---

To set a tint, go to the **Edit Menu** (or Unity Menu) and select **Preferences**. Choose the **Colours** menu and find the property called **Playmode tint**.

Click on the existing colour to see a colour wheel where you can choose a colour and opacity level:

![The colour wheel pop-up window with a blue medium opacity tint selected.](images/tint-colour-window.png){:width="400px"}

**Tip:** Try a light colour so that you can still clearly see the text in the editor when the scene is running.

Return to the Unity Editor and press the **Play** button to see your new tint in action. When you are happy with the tint you have chosen, press the **Play** button again to exit Play mode.

--- /task ---

The Character Controller component provides a `SimpleMove` method.

--- task ---

**Add** code to use the vertical input value to move the Player each frame.

You can **remove** the Debug code.

A Unity `Vector3` is used to store 3D points or directions. The `forward` variable stores the direction that the Player is facing:

--- code ---
---
language: cs filename: PlayerController.cs - Update() line_numbers: true line_number_start: 14
line_highlights: 18-23
---

    void Update()
    {
        float speed = Input.GetAxis("Vertical");
    
        // Forward is the forward direction for this character
        Vector3 forward = transform.TransformDirection(Vector3.forward);
    
        // You need the Character Controller so you can use SimpleMove
        CharacterController controller = GetComponent<CharacterController>();
        controller.SimpleMove(forward * speed);
    }
--- /code ---

--- /task ---

--- task ---

**Test:** Klik op **Play** om de afspeelmodus te openen en je code uit te proberen. Gebruik de <kbd>W</kbd> en <kbd>S</kbd> toetsen of de pijltjestoetsen omhoog en omlaag om naar voren en naar achteren te schuiven.

**Debug:** Vergeet niet om het Console venster te controleren op nuttige berichten. Controleer zorgvuldig haakjes, puntkomma's en hoofdletters in de code.

**Tip:** Make sure your mouse pointer is in the **Game view**.

Try and walk through the wall. De `SimpleMove` methode van de Character Controller component zorgt ervoor dat je niet door GameObjects kunt lopen die een collider hebben. Een collider wordt automatisch toegevoegd wanneer je een 3D-vorm maakt zoals je dat deed voor de muur.

Je kunt in de scèneweergave "pannen" door de rechtermuisknop ingedrukt te houden en te verslepen. Pan om een beter zicht op de muur te krijgen terwijl je personage er tegenaan loopt:

![Scene and Game views of the character stopped at the wall.](images/player-wall.gif){:width="500px"}

To move your Player, move the mouse pointer back to the **Game view**.

Click the **Play** button again to exit Play mode.

--- /task ---

--- task ---

Voeg nog een regel toe zodat je personage kan `draaien` wanneer de speler op de toetsen <kbd>A</kbd> en <kbd>D</kbd> of de pijltjestoetsen links en rechts drukt:

--- code ---
---
language: cs filename: PlayerController.cs - Update() line_numbers: true line_number_start: 14
line_highlights: 18-19
---

    void Update()
    {
        float speed = Input.GetAxis("Vertical");
    
        // Rotate around y-axis
        transform.Rotate(0, Input.GetAxis("Horizontal"), 0);
    
        // Forward is the forward direction for this character
        Vector3 forward = transform.TransformDirection(Vector3.forward);
    
        // You need the Character Controller so you can use SimpleMove
        CharacterController controller = GetComponent<CharacterController>();
        controller.SimpleMove(forward * speed);
    }
--- /code ---

Sla je code op en schakel terug naar de Unity Editor. Unity zal je bijgewerkte script laden.

--- /task ---

--- task ---

**Test:** Click **Play** to enter Play mode and try out your code. Gebruik de <kbd>A</kbd> en <kbd>D</kbd> toetsen of de linker- en rechterpijltjestoetsen om je personage te laten draaien.

**Debug:** als je nog steeds uitvoer naar de console ziet en beweging niet werkt, zorg er dan voor dat je het script in de code-editor hebt opgeslagen.

Click the **Play** button again to exit Play mode.

--- /task ---

Je kunt ook de snelheid van beweging en rotatie regelen.

--- task ---

Open je PlayerController script en voeg variabelen toe voor `moveSpeed` en `rotateSpeed`.

--- code ---
---
language: cs filename: PlayerController.cs line_numbers: true line_number_start: 5
line_highlights: 7-8
---
public class PlayerController : MonoBehaviour
{ public float moveSpeed = 4.0f; //The f at the end of the number says it is a floating-point number public float rotateSpeed = 1.5f;

    // Start is called before the first frame update
    void Start()
    {
--- /code ---

--- /task ---

--- task ---

Update de code voor `Rotate` en `SimpleMove` om de nieuwe variabelen te gebruiken:

--- code ---
---
language: cs filename: PlayerController.cs - Update() line_numbers: true line_number_start: 21
line_highlights: 22
---

        // Rotate around y-axis
        transform.Rotate(0, Input.GetAxis("Horizontal") * rotateSpeed, 0);
--- /code ---

and

--- code ---
---
language: cs filename: PlayerController.cs - Update() line_numbers: true line_number_start: 27
line_highlights: 29
---

        // You need the Character Controller so you can use SimpleMove
        CharacterController controller = GetComponent<CharacterController>();
        controller.SimpleMove(forward * speed * moveSpeed);
--- /code ---

--- /task ---

--- task ---

**Test:** Speel je scène en controleer of je tevreden bent met de snelheidsinstellingen.

Breng wijzigingen aan in `moveSpeed` en `rotateSpeed` in je script totdat je tevreden bent.

**Tip:** je kunt de `Debug.Log()` regels verbergen door `//` aan het begin van de regel te zetten. Je kunt ook meerdere regels verbergen met `/*` en `*/`:
```
        /*if (speed != 0) // Player moving
        {
            Debug.Log(speed);
        }*/
```

Click the **Play** button again to exit Play mode.

--- /task ---

--- save ---
