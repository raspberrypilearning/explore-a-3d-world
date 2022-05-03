
--- question ---

---
legend: Question 3 of 3
---

This Script is supposed to print the Player’s vertical movement value each frame, but it only prints it once at the start. How could you fix this?

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

- ( ) Change the code to `Debug.log(speed);`

  --- feedback ---

  No. C# is case sensitive so you need to make sure to use capital letters correctly. The C# naming convention is to capitalise all words in a method name so `Debug.Log(speed);` is correct.

  --- /feedback ---

- ( ) Add a semi-colon to the end of the `Debug` line


  --- feedback ---

That's not it. Forgetting to add a semi-colon `;` to the end of a line is a common mistake in C#, but this code does have a semi-colon at the end of the line.

  --- /feedback ---

- ( ) Drag the script to the Player GameObject in the Inspector

  --- feedback ---

  That's not it. It's easy to forget to attach a new script to a GameObject, but the code is running once so that's not the problem here.

  --- /feedback ---

- (x) Move the code from the `Start` method to the `Update` method

  --- feedback ---

  Yes! The `Debug.Log(speed);` line is in the `Start` method, which only runs once, before the first frame. Moving the code to the `Update` method will run the code every frame so the Player's vertical position will keep printing.

  --- /feedback ---

--- /choices ---

--- /question ---
