# Version 2.1.3

![TARDIS Refined](tardis_refined_v2_1.png)

#### Bug Fixes
- Bug Fix: Placing and entering TARDIS door in the overworld crashes the game with Immersive Portals [#444](https://github.com/WhoCraft/TardisRefined/issues/444)
- Bug Fix: Players can land TARDIS within TARDIS with Landing Pad [#447](https://github.com/WhoCraft/TardisRefined/issues/447)
- Bug Fix: Fixed TARDIS not storing Adventure Mode Dimensions correctly
- Bug Fix: Fixed Dedicated Servers on Fabric having issues loading data from disk (Caused dupe TARDIS and loss of Upgrades etc)
- Bug Fix: Fixed Diagonal Windows Support
- Bug fix: Fixed duplication happening on logging out mid-flight (and other occasions)
- Bug fix: Fixed issue where End Dragon fight would not be checked correctly
- Bug fix: Potentially fixed interior door messing up on AMD cards!

#### Config
- Added use_internal_shaders client config
- Added render_vortex_in_door client config

#### Interiors
- Added Panamax Interior

#### Textures and Models
- Altered: Factory Console Emission Texture
- Altered: Factory Console (Mint) Emission Texture
- Altered: Factory Console (Vintage) Emission Texture
- Altered: Factory Console (Wood) Emission Texture
- Added: Victorian Console (Default) Emission Texture
- Added: Victorian Console (Bronze Age) Emission Texture

#### API Changes
- Addon mods can now freely register console models
- Addon mods consoles can now have per variant models