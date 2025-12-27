# PC3D - First-Person 3D Game Framework

A complete Unity-based first-person game framework built on Unity's Starter Assets, featuring full 3D character control, physics interactions, and a rich collection of game assets.

## 🎮 Features

### Core Gameplay Systems
- **First-Person Controller** - Smooth, responsive character movement with walking and sprinting
- **Jump & Fall Mechanics** - Realistic gravity simulation with configurable jump height
- **Ground Detection** - Accurate grounded state for proper physics interactions
- **Camera System** - Cinemachine-powered camera with smooth look mechanics
- **Physics-Based Pushing** - Push interactive objects in the world

### Input Systems
- **Modern Input System** - Full support for Unity's new Input System
- **Keyboard & Mouse** - Desktop controls with mouse look
- **Controller Support** - Gamepad/analog stick support
- **Mobile Controls** - Touch-based joysticks and buttons for mobile platforms

### Graphics & Rendering
- **Universal Render Pipeline (URP)** - Modern rendering pipeline for better performance
- **Stylized Visuals** - Low-poly aesthetic with Polygon assets from SyntyStudios
- **Advanced Rendering** - Support for various rendering features and effects

### Asset Collections
- **Polygon Characters** - Multiple character models (cop, cowboy, female, etc.)
- **Polygon Buildings** - Modular building pieces and structures
- **Polygon Vehicles** - Cars, planes, and other vehicles
- **Polygon Props** - Weapons, tools, furniture, and environmental objects
- **Stylized Grass** - High-quality vegetation system
- **Terrain Systems** - Pre-built terrain with textures and heightmaps

### Development Tools
- **Houdini Engine Integration** - Procedural geometry generation and asset creation
- **Mobile Optimization** - Built-in mobile performance optimization
- **Adaptive Performance** - Dynamic quality scaling

## 📋 Requirements

- **Unity 2021.3 LTS** or newer
- **Universal Render Pipeline (URP)** enabled
- **Input System Package** installed
- Recommended: 8GB RAM, GPU with 2GB+ VRAM

## 🚀 Getting Started

### Clone the Repository
```bash
git clone https://github.com/vishal-crypto/pc3d.git
cd pc3d
```

### Open in Unity
1. Open Unity Hub
2. Add project folder
3. Select Unity 2021.3 LTS or newer
4. Wait for dependencies to import (Houdini Engine, assets, etc.)

### Run the Demo Scene
1. Open `Assets/Scenes/SampleScene.unity`
2. Press Play (Ctrl+P)
3. Use **WASD** to move, **Space** to jump, **Shift** to sprint, **Mouse** to look around

## 🎮 Controls

| Action | Input |
|--------|-------|
| Move Forward | W |
| Move Backward | S |
| Strafe Left | A |
| Strafe Right | D |
| Jump | Space |
| Sprint | Left Shift |
| Look Around | Mouse Move |
| Lock/Unlock Cursor | Click |

### Mobile Controls
- Left joystick for movement
- Right joystick for camera look
- Virtual buttons for jump and sprint

## 📁 Project Structure

```
Assets/
├── StarterAssets/           # Core first-person controller
│   ├── FirstPersonController/
│   ├── InputSystem/
│   ├── Mobile/
│   └── Environment/
├── SyntyStudios/            # Polygon assets
│   ├── PolygonPrototype/    # Main asset pack
│   ├── PolygonStarter/      # Additional assets
│   └── PolygonSamples/      # Sample scenes
├── StylizedGrass/           # Vegetation
├── Plugins/                 # Houdini Engine
├── Scenes/                  # Game scenes
└── TutorialInfo/            # Documentation
```

## 🛠️ Customization

### Adjust Player Speed
In the Scene, select the Player object and modify:
- **Move Speed** - Normal walking speed (default: 4 m/s)
- **Sprint Speed** - Running speed (default: 6 m/s)
- **Jump Height** - Jump height in meters (default: 1.2)
- **Gravity** - Gravity strength (default: -15)

### Add New Assets
1. Import models/prefabs into Assets folder
2. Create new scenes in `Assets/Scenes/`
3. Reference existing FirstPersonController for consistency

### Mobile Build Settings
1. Go to File > Build Settings
2. Add scenes you want in build
3. Select Android or iOS platform
4. Configure mobile input in Mobile folder scripts

## 📦 Included Asset Packs

### SyntyStudios - Polygon Series
- **PolygonPrototype** - Core assets for prototyping
- **PolygonStarter** - Beginner-friendly assets
- **PolygonSciFiCity** - Sci-fi themed objects
- **PolygonDungeons** - Fantasy dungeon pieces

Each pack includes:
- Models (characters, buildings, props, vehicles)
- Materials and textures
- Prefabs ready to use
- Lighting settings

## 🎨 Rendering Pipeline

This project uses **Universal Render Pipeline (URP)** for:
- Better performance on mobile devices
- Support for both 2D and 3D
- Faster iteration and customization
- Better post-processing options

Configure URP settings in:
`Assets/Settings/UniversalRenderPipelineGlobalSettings.asset`

## 🔧 Scripting Reference

### FirstPersonController.cs
Handles player movement, jumping, and camera control
```csharp
public float MoveSpeed = 4.0f;      // Walking speed
public float SprintSpeed = 6.0f;    // Running speed
public float JumpHeight = 1.2f;     // Jump height
public float Gravity = -15.0f;      // Gravity value
```

### StarterAssetsInputs.cs
Manages all input from keyboard, mouse, and gamepad
```csharp
public Vector2 move;        // WASD input
public Vector2 look;        // Mouse/stick look
public bool jump;           // Space/A button
public bool sprint;         // Shift/LS+RS
```

### BasicRigidBodyPush.cs
Allows player to push physics objects
```csharp
public float strength = 1.1f;       // Push force
public LayerMask pushLayers;        // Which layers to push
```

## 📚 Documentation

- Full documentation: `Assets/StarterAssets/StarterAssets_Documentation_v1.1.pdf`
- License info: `Assets/StarterAssets/license.txt`

## 🐛 Troubleshooting

**"Missing dependencies" error?**
- Go to Tools > Starter Assets > Reinstall Dependencies

**Input not working?**
- Ensure Input System package is installed
- Check that your scene has a PlayerInput component

**Mobile input not responding?**
- Verify UI Canvas is set up correctly
- Check Virtual Input prefabs are in your scene

**Houdini Engine not found?**
- You can remove `Assets/Plugins/HoudiniEngineUnity/` if not needed
- Restart Unity after removal

## 🎓 Learning Resources

- [Unity First Person Controller Tutorial](https://learn.unity.com/)
- [Cinemachine Documentation](https://docs.unity3d.com/Packages/com.unity.cinemachine@latest)
- [Universal Render Pipeline Guide](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal/latest)
- [SyntyStudios Asset Documentation](https://www.syntystudios.com/)

## 📝 License

This project uses:
- **StarterAssets** - Unity provided (See `Assets/StarterAssets/license.txt`)
- **Polygon Assets** - SyntyStudios (Requires separate license)
- **Houdini Engine** - Side Effects Software (Requires separate license)

Ensure you have proper licenses for all included assets if you plan to publish.

## 🚀 What's Next?

### Beginner Tasks
- [ ] Customize player appearance
- [ ] Add new scenes and environments
- [ ] Place assets in your world
- [ ] Create basic game mechanics

### Intermediate Tasks
- [ ] Add enemy AI
- [ ] Implement inventory system
- [ ] Create dialogue system
- [ ] Add particle effects

### Advanced Tasks
- [ ] Multiplayer networking
- [ ] Advanced physics
- [ ] Procedural generation with Houdini
- [ ] Console/mobile optimization

## 💬 Support

For issues with:
- **StarterAssets** - Check Unity documentation
- **Polygon Assets** - Visit SyntyStudios website
- **Houdini Engine** - Contact Side Effects Software
- **Input System** - See Unity Input System docs

## 📦 Repository

**GitHub:** https://github.com/vishal-crypto/pc3d

---

**Happy Game Development! 🎮**
