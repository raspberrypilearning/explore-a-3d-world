
--- question ---

---
legend: Vraag 3 van 3
---

Dit script zou de waarde van de verticale beweging van de speler per frame moeten afdrukken, maar het print het slechts eenmaal aan het begin. Hoe kun je dit oplossen?

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        float speed = Input.GetAxis("Vertical");
        Debug.Log(speed);
    }

    // Update is called once per frame
    void Update()
    {

    }
}
```

--- choices ---

- ( ) Wijzig de code in `Debug.log(speed);`

  --- feedback ---

  Nee. C# is hoofdlettergevoelig, dus je moet ervoor zorgen dat je hoofdletters correct gebruikt. De naamgevingsconventie van C# is om alle woorden in een methodenaam een hoofdletter te geven, zodat `Debug.Log(speed);` correct is.

  --- /feedback ---

- ( ) Voeg een puntkomma toe aan het einde van de regel `Debug`


  --- feedback ---

Dat is niet juist. Vergeten om een puntkomma `;` toe te voegen aan het einde van een regel is een veel voorkomende fout in C#, maar deze code heeft een puntkomma aan het einde van de regel.

  --- /feedback ---

- ( ) Sleep het script naar het Spelersobject in de Inspector

  --- feedback ---

  Dat is niet juist. Het is makkelijk om te vergeten om een nieuw script aan een GameObject te koppelen, maar de code wordt eenmaal uitgevoerd, dus dat is hier niet het probleem.

  --- /feedback ---

- (x) verplaats de code van de `Start` methode naar de `Update` methode

  --- feedback ---

  Ja! De regel `Debug.Log(speed);` staat in de `Start` methode, die slechts eenmaal wordt uitgevoerd, voor het eerste frame. Door de code naar de `Update` methode te verplaatsen, wordt de code elk frame uitgevoerd, zodat de verticale positie van de speler blijft afdrukken.

  --- /feedback ---

--- /choices ---

--- /question ---
