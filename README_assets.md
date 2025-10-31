# Blade Assets Repository

## Overview

This repository contains demo assets and resources for the Blade SDK platform. All assets are designed for compatibility with Raku SDK and optimized for AR experiences.

## Repository Structure

```
blade-assets/
├── demos/
│   ├── Space_Battleship_Defense.zip - Complete demo package with assets and documentation
│   └── Space_Battleship_Defense.mp4 - Demo video
└── README_assets.md - This file
```

## SDK Compatibility

### Raku SDK

All assets in this repository are compatible with and optimized for the **Raku SDK** platform. The assets support:

- **Raku Hardware**: AR glasses and devices running the Raku platform
- **Performance Targets**: 60 FPS sustained on Raku hardware
- **Platform Features**: Spatial anchors, gaze-based tracking, multiplayer networking

### Space Battleship Defense Demo

The Space Battleship Defense demo is a cooperative AR tower defense game featuring:

- 60-second defense loops with escalating enemy waves
- Multiplayer support (1-4 players) with host/client architecture
- Optimized for Raku (MiRZA) AR glasses
- Epic superweapon finale sequence

#### Package Contents

The `Space_Battleship_Defense.zip` package contains:

**Documentation**:
- Complete design specification
- Asset specifications and requirements
- Telemetry implementation details
- Public gameplay storyboard
- Visual assets documentation

**Unity Assets**:
- C# scripts for game logic and audio control
- Prefabs for game objects (enemies, battleship, projectiles)
- 3D models and meshes (OBJ and FBX formats)
- Textures and concept art
- Audio files (sound effects and background music)
- Visual effects and materials

**Visual Assets**:
- SVG thumbnails for all game entities
- Storyboard assets
- UI elements and placeholders

## Usage

### Downloading Assets

Assets can be accessed directly from this repository:

```bash
# Download Space Battleship Defense package
curl -L -O https://raw.githubusercontent.com/BladeWireless/blade-assets/main/demos/Space_Battleship_Defense.zip

# Extract the package
unzip Space_Battleship_Defense.zip
```

### Integration with Unity

1. Download the Space Battleship Defense package
2. Extract the ZIP file
3. Review the documentation in the `docs/` directory
4. Import Unity assets from `Assets/SpaceBattleshipDefense/` into your Unity project
5. Follow the integration guidelines in the included documentation

## Version History

| Date | Version | Changes |
|------|---------|---------|
| 2025-10-31 | 1.1 | Updated asset metadata for Raku SDK rebrand - replaced AR1+/AR2 references with Raku |
| 2025-10-15 | 1.0 | Initial release with Space Battleship Defense demo package |

## Raku Rebrand Update (2025-10-31)

As part of the Raku SDK rebrand initiative, all asset metadata has been updated to reflect the new platform naming:

- **Legacy References Removed**: AR1+ and AR2 hardware references
- **Updated To**: Raku platform and SDK compatibility
- **Files Updated**: All documentation within Space_Battleship_Defense.zip package
- **Compatibility**: Full backward compatibility maintained for Raku devices

## Support

For questions or issues related to the assets in this repository:

- Review the included documentation files in each package
- Consult the main SDK repository: https://github.com/BladeWireless/blade-sdk
- Check the demos documentation for specific implementation guidance

## License

All assets are proprietary to BladeWireless unless otherwise noted. Individual asset licenses are documented within each package in the `licenses/asset_licenses.yaml` file (if present).

Some assets use third-party components with the following licenses:
- **Fonts**: Apache 2.0 (Roboto Mono) / SIL OFL 1.1 (Orbitron)
- **Audio SFX**: Freesound.org CC0/CC-BY (see individual credits)
- **Models**: BladeWireless Internal / CC0 (Modified where noted)

## Contributing

This repository is managed by BladeWireless. For contribution guidelines or to report issues, please contact the SDK team via the main blade-sdk repository.
