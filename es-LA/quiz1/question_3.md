
--- question ---

---
legend: Pregunta 3 de 3
---

Se supone que este Script muestra el valor de movimiento vertical del jugador en cada cuadro, pero solo lo muestra una vez al principio. ¿Cómo podrías arreglarlo?

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

- (x) Mueva el código del método `Inicio` al método `Actualizar`

  --- feedback ---

  ¡Sí! La línea `Debug.Log(velocidad);` está en el método `Inicio`, que solo se ejecuta una vez, antes del primer cuadro. Mover el código al método `Actualización` ejecutará el código en cada cuadro, por lo que siempre se mostrará la posición vertical actual del jugador.

  --- /feedback ---

--- /choices ---

--- /question ---
