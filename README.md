# Parallax Scrolling Unity

Efeito de movimento do segundo plano da cena.

Quando mais longe o objeto, mais lento ele se movimenta.

```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class ScrollH : MonoBehaviour
{
    public float vel = 0.1f;
    public Renderer quad;

    void Update()
    {
        Vector2 offset = new Vector2(vel * Time.deltaTime, 0);
        quad.material.mainTextureOffset += offset;
    }
}
```
