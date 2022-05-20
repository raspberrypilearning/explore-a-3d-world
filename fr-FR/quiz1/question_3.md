
--- question ---

---
legend: Question 3 sur 3
---

Ce script est censé imprimer la valeur de mouvement vertical du joueur à chaque frame, mais il ne l'imprime qu'une seule fois au début. Comment pourrais-tu régler cela ?

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

- ( ) Remplace le code par `Debug.log(speed);`

  --- feedback ---

  Non. C# est sensible à la casse, tu dois donc t'assurer d'utiliser correctement les majuscules. La convention de dénomination C# consiste à mettre en majuscule tous les mots dans un nom de méthode, donc `Debug.Log(speed);` est correct.

  --- /feedback ---

- ( ) Ajoute un point-virgule à la fin de la ligne `Debug`


  --- feedback ---

Ce n'est pas ça. Oublier d'ajouter un point-virgule `;` à la fin d'une ligne est une erreur courante en C#, mais ce code a un point-virgule à la fin de la ligne.

  --- /feedback ---

- ( ) Fais glisser le script vers le Player GameObject dans l'Inspector

  --- feedback ---

  Ce n'est pas ça. Il est facile d'oublier d'attacher un nouveau script à un GameObject, mais le code s'exécute une fois, ce n'est donc pas le problème ici.

  --- /feedback ---

- (x) Déplace le code de la méthode `Start` vers la méthode `Update`

  --- feedback ---

  Oui ! La ligne `Debug.Log(speed);`est dans la méthode `Start`, qui ne s'exécute qu'une seule fois, avant la première frame. Déplacer le code vers la méthode `Update` exécutera le code à chaque frame afin que la position verticale du joueur continue à s'imprimer.

  --- /feedback ---

--- /choices ---

--- /question ---
