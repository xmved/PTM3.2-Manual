# *DEV_MANUAL_SERVER_02*

Используется блокировка частей интерфейса
```csharp
using UnityEngine;

namespace xmved.general

public class UIBlocker : MonoBehaviour

{

    private GameObject blockerObject; 


    public void ShowBlocker()

    {

        if (blockerObject != null) return;

        blockerObject = new GameObject("UIBlocker");

        blockerObject.transform.SetParent(transform, false);

        RectTransform rectTransform = blockerObject.AddComponent<RectTransform>();

        rectTransform.anchorMin = Vector2.zero;

        rectTransform.anchorMax = Vector2.one;

        rectTransform.sizeDelta = Vector2.zero;

        rectTransform.anchoredPosition = Vector2.zero;

        
        blockerObject.AddComponent<CanvasRenderer>();

        
        UnityEngine.UI.Image image = blockerObject.AddComponent<UnityEngine.UI.Image>();

        image.color = new Color(0, 0, 0, 0.5f);


        blockerObject.AddComponent<UnityEngine.UI.GraphicRaycaster>();

    }


    public void HideBlocker()

    {

        if (blockerObject != null)

        {

            Destroy(blockerObject);

            blockerObject = null;

        }

    }

}
```
