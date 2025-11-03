# Raku Assets Repository

## Overview

This repository contains demo assets and resources for the Raku SDK platform. All assets are designed for compatibility with Raku SDK and optimized for AR experiences.

## Repository Structure

```
raku-assets/
├── demos/
│   ├── Space_Battleship_Defense.zip - Complete demo package with assets and documentation
│   └── Space_Battleship_Defense.mp4 - Demo video
├── README.md - This file
└── MIGRATION.md - Asset migration guide for dependent repositories
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
curl -L -O https://raw.githubusercontent.com/BladeWireless/raku-assets/main/demos/Space_Battleship_Defense.zip

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
| 2025-11-03 | 1.2 | Repository rebrand complete - renamed to raku-assets with migration guide |
| 2025-10-31 | 1.1 | Updated asset metadata for Raku SDK rebrand - replaced AR1+/AR2 references with Raku |
| 2025-10-15 | 1.0 | Initial release with Space Battleship Defense demo package |

## Raku Rebrand

As part of the Raku SDK rebrand initiative, this repository has been rebranded from `blade-assets` to `raku-assets`:

- **Repository Name**: Updated from `blade-assets` to `raku-assets`
- **Asset Metadata**: All references updated from AR1+/AR2 to Raku SDK
- **Platform References**: Updated to Raku platform and SDK compatibility
- **Documentation**: Complete rebrand documentation and migration guide included
- **Compatibility**: Full backward compatibility maintained for Raku devices

See [MIGRATION.md](./MIGRATION.md) for guidance on updating references to this repository.

## Support

For questions or issues related to the assets in this repository:

- Review the included documentation files in each package
- Consult the main SDK repository: https://github.com/BladeWireless/raku-sdk
- Check the demos documentation for specific implementation guidance

## License

All assets are proprietary to BladeWireless unless otherwise noted. Individual asset licenses are documented within each package in the `licenses/asset_licenses.yaml` file (if present).

Some assets use third-party components with the following licenses:
- **Fonts**: Apache 2.0 (Roboto Mono) / SIL OFL 1.1 (Orbitron)
- **Audio SFX**: Freesound.org CC0/CC-BY (see individual credits)
- **Models**: BladeWireless Internal / CC0 (Modified where noted)

## Contributing

This repository is managed by BladeWireless. For contribution guidelines or to report issues, please contact the SDK team via the main raku-sdk repository.
