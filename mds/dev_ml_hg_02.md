# *DEV_MANUAL_HG_02*

Загрузите компоненты **Hangar_Camera_Scripts** в папку с **C#_Scripts**


<img src="null#moving_hcs_to_cs"/>

#

Важное примечание! Если Вы уже ранее загружали компоненты **Hangar_Camera_Scripts**
то стоит обратить внимание на текстовый документ **ChangeDZ** где Вы можете увидеть
все изменения новых версий.

<img src="null#see_chGZ"/>

> Такие как:
> 
> DeploymentOfSmooth v(0.9.37b)
>
> HangarCameraRotateType (1)
>
> HangarCameraPoints (def 1)


> [!TIP]
> Обычно больше одной точки в  HangarCameraPoints используется
> для отображения других объектов от основного.


#


Настройки такие как **Horizontal_Speed**/**Vertical_Speed** не используются за место них применяется модификатор **multiple**

Также не применяется аргумент **AllowSwitchRotateType** заменяется как
```csharp
public scroll;
[Range(0, 2)] public switchType = 1;
```

#

Для загрузки камеры достаточно оставить одну точку для всех танков.
Распаковка танков в ангаре является другой группой нежели для подготовленных к бою машин.

```csharp
Load.Prefab = null;
// if argument
```
