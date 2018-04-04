# RaionMobileInputAnalogLibrary
Virtual Game Analog Library for Unity
  
![Generic badge](https://img.shields.io/badge/Version-v1.0.0-green.svg)
![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)

## Screenshots
<p align="center">
  <img src="https://raw.githubusercontent.com/jmsrsd/RaionMobileInputAnalog/master/Screenshots/Screenshot.00.gif" height="320"/>
</p>

## Installation
1. Download the \*.unitypackage file(s) in Build dir or in "Build Link" section of this page
2. Open the \*.unitypackage file(s)
3. Click "All" button and then import button in Unity import package dialogue
4. Read "Usage" section of this page to know how to use the library

## Build Link
[.unitypackage](https://github.com/jmsrsd/MobileInputAnalog/raw/master/Build/Raion.MobileInputAnalog.unitypackage)  
[.apk](https://github.com/jmsrsd/RaionMobileInputAnalog/raw/master/Build/apk/Raion.AnalogTouchInput.Test.apk)
  
## Dir structure
```
Assets
├───raion
│   └───MobileInputAnalog
│       ├───Materials
│       │       Raion.MobileInputAnalog.Material.Standard.Gray.mat
│       │       Raion.MobileInputAnalog.Material.Standard.White.mat
│       │
│       └───Scripts
│               MobileInputAnalog.cs
│               MobileInputAnalogCanvas.cs
│               MobileInputAnalogHelper.cs
│               MobileInputAnalogUI.cs
│               MobileInputAnalogUIBackground.cs
│               MobileInputAnalogUIForeground.cs
│               TestMobileInputAnalog.cs
│
└───Resources
    └───raion
        └───MobileInputAnalog
            └───Sprites
                    Raion.MobileInputAnalog.Sprite.Circle.png
```
  
## Usage
To initialize the library:
```
raion.MobileInputAnalog.GetInstance();
```

To use the library:
```C#
using UnityEngine;

public class LibraryTest : MonoBehaviour {
  private void Update() {
    float speed = 10.0f;

    Vector2 direction =
      raion.MobileInputAnalog.Library.GetInstance().GetDirection();

    Vector3 velocity = Vector3.zero;
    velocity.x = direction.x;
    velocity.z = direction.y;

    // Moving the GameObject
    transform.position += velocity * speed * Time.deltaTime;
  }
}

```
