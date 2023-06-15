
--- question ---

---
القائمة: السؤال 3 من 3
---

من المفترض أن يقوم هذا البرنامج النصي بطباعة قيمة الحركة العمودية للاعب لكل إطار ، ولكنه يطبعها مرة واحدة فقط في البداية. كيف يمكنكم اصلاح هذا؟

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

- () قم بتغيير الكود إلى `Debug.log (السرعة) ؛`

  --- feedback ---

  لا. C # حساس لحالة الأحرف ، لذا عليك التأكد من استخدام الأحرف الكبيرة بشكل صحيح. اصطلاح التسمية C # هو جعل كل الكلمات بأحرف كبيرة في اسم الطريقة بحيث تكون `Debug.Log (السرعة) ؛` صحيح.

  --- /feedback ---

- () أضف فاصلة منقوطة إلى نهاية السطر `Debug`


  --- feedback ---

هذا ليس هو. نسيان إضافة فاصلة منقوطة `؛` في نهاية السطر هو خطأ شائع في C # ، لكن هذا الرمز يحتوي على فاصلة منقوطة في نهاية السطر.

  --- /feedback ---

- () اسحبوا النص إلى Player GameObject في المفتش

  --- feedback ---

  هذا ليس هو. من السهل أن تنسى إرفاق برنامج نصي جديد بكائن GameObject ، لكن الكود يعمل مرة واحدة لذا فهذه ليست المشكلة هنا.

  --- /feedback ---

- (x) انقل الكود من طريقة `Start` إلى طريقة `Update`

  --- feedback ---

  نعم! `Debug.Log (السرعة) ؛ يوجد سطر` في طريقة `Start` ، والتي تعمل مرة واحدة فقط ، قبل الإطار الأول. سيؤدي نقل الكود إلى طريقة `Update` إلى تشغيل الكود في كل إطار حتى يستمر الوضع الرأسي للاعب في الطباعة.

  --- /feedback ---

--- /choices ---

--- /question ---
