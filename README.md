# Pelly
Tools for Unity

Simulates the "A" key press every 0.6 seconds:
```cs
using UnityEngine;

using Pelly.OS;

public class test : MonoBehaviour
{
    private float action = 0.0f;
    private float period = 0.6f;

    private void Start()
    {
        Application.runInBackground = true;
    }

    private void Update()
    {
        if (Time.time > action)
        {
            action += period;
            Windows.KeyPress(Pelly.KeyCode.KEY_A);
        }
    }
}

```
