
--- question ---

---
legend: Pregunta 3 de 3
---

Se supone que este Script muestra el valor de movimiento vertical del jugador en cada cuadro, pero solo lo muestra una vez al principio. ¿Cómo podrías arreglarlo?

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ControladorJugador : MonoBehaviour
{
    // Start se llama antes de la actualización del primer cuadro
    void Start()
    {
        float velocidad = Input.GetAxis("Vertical");
        Debug.Log(velocidad);
    }

    // Update se llama una vez por cada cuadro.
    void Update()
    {

    }
}
```

--- choices ---

- ( ) Cambie el código a `Debug.log(velocidad);`

  --- feedback ---

  No. C# distingue entre mayúsculas y minúsculas, por lo que debe asegurarse de usar las letras mayúsculas correctamente. La convención de nomenclatura de C# es poner en mayúscula el inicio de todas las palabras en el nombre del método, por lo que `Debug.Log(velocidad);` es correcto.

  --- /feedback ---

- ( ) Agregue un punto y coma al final de la línea `Debug`


  --- feedback ---

Eso no es correcto. Olvidarse de agregar un punto y coma `;` al final de una línea es un error común en C#, pero este código tiene un punto y coma al final de la línea.

  --- /feedback ---

- ( ) Arrastre las instrucciones de codigo del Script al Objeto del juego Jugador en el Inspector

  --- feedback ---

  Eso no es correcto. Es fácil olvidar adjuntar las nuevas instrucciones de codigo del script a un Objeto del juego, pero el código se ejecuta una vez, así que ese no es el problema aquí.

  --- /feedback ---

- (x) Mueva el código del método `Start` al método `Update`

  --- feedback ---

  ¡Sí! La línea `Debug.Log(velocidad);` está en el método `Start`, que solo se ejecuta una vez, antes del primer cuadro. Mover el código al método `Update` ejecutará el código en cada cuadro, por lo que siempre se mostrará la posición vertical actual del jugador.

  --- /feedback ---

--- /choices ---

--- /question ---
