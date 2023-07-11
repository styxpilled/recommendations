This is a list containing all of the instructions to more-or-less replicate my setup as of 02.2023. 
I'll update this with links and explanations in the future.

- [GLOSSARY](#glossary)
- [SHELL](#shell)
- [PROGRAMS](#programs)
- [BROWSER EXTENSIONS](#browser-extensions)
- [DISCORD](#discord)
  - [PLUGINS](#plugins)
  - [THEMES](#themes)
- [MINECRAFT](#minecraft)
  - [GLOSSARY](#glossary-1)
  - [BACKEND](#backend)
  - [PERFORMANCE](#performance)
  - [RENDERING](#rendering)
  - [UI](#ui)
  - [MISC](#misc)
  - [BUILDING](#building)
  - [RESOURCE PACKS](#resource-packs)
  - [SHADERS](#shaders)
  - [DEVELOPMENT](#development)

## GLOSSARY

- You should probably install them in the order you see them.
- `?` prefix means I either don't like this option and suggest finding an alternative in the future, or see this as something optional in general.
- `$` prefix means this is proprietary || closed source software. 
- [Winget](https://github.com/microsoft/winget-cli) is a package manager for Windows that should come pre-installed. Otherwise download it from the [Microsoft Store](https://www.microsoft.com/p/app-installer/9nblggh4nns1).

## SHELL

- [Windows Terminal](https://learn.microsoft.com/en-us/windows/terminal/install)
- [curl](https://curl.se/)
  - `winget install cURL.cURL`
  - According to [their website](https://curl.se/windows/microsoft.html), Windows ships with curl. It's just that Powershell has a `curl` alias. In that case, use `curl.exe` until you have `nushell` installed.
- [rustup](https://rustup.rs/)
  - `winget install rustup`
- [git](https://git-scm.com/downloads)
  - `winget install Git.Git`
- [gsudo](https://github.com/gerardog/gsudo)
  - `winget install gsudo`
- [cargo-binstall](https://github.com/cargo-bins/cargo-binstall)
  - Downloading their release is better than using `cargo install cargo-binstall` because they optimize more.
  - You probably need one of the C++ redistributables.
- [nushell](https://github.com/nushell/nushell)
  - `winget install nushell`
  - `cargo binstall nu`
- [pnpm](https://pnpm.io/installation)
  - `iwr https://get.pnpm.io/install.ps1 -useb | iex`
  - Use `pnpm` to manage your `Node` versions.
- [Python](https://www.python.org/downloads/)
  - Use version < 3.10.
  - [Poetry](https://python-poetry.org/docs/)
    - Most reasonable but doesn't work with `pytorch` custom CUDA / CUDNN stuff.
  - [pipenv](https://github.com/pypa/pipenv)
    - Worse but works with `pytorch`.
- [lld](https://releases.llvm.org/)
  - Faster linker for `Rust`.
  - Might be default in future versions
- [ohmyposh](https://ohmyposh.dev/docs/installation/windows)
  - `winget install JanDeDobbeleer.OhMyPosh -s winget`
  - Run `oh-my-posh font install` and select DroidSans.
- [zoxide](https://github.com/ajeetdsouza/zoxide)
  - `winget install zoxide`
  - `cargo binstall zoxide`
- [ffmpeg / ffprobe](https://www.ffmpeg.org/download.html)
  - `winget install --id Gyan.FFmpeg`
- [yt-dlp](https://github.com/yt-dlp/yt-dlp/releases)
- [fzf](https://github.com/junegunn/fzf)
  - `winget install fzf`
- ?[Deno](https://github.com/denoland/deno)
  - `winget install --id DenoLand.Deno`
- [ImageMagick](https://imagemagick.org/script/download.php)
  - Winget:
    - `winget install imagemagick`
- ?[Ghostscript](https://www.ghostscript.com/releases/index.html)

## PROGRAMS

- [Firefox](https://www.mozilla.org/en-US/firefox/new/)
  - `Chromium` has problems and doesn't work as well as Chrome.
  - Never use or install Brave.
  - Refer to the [extensions section](#browser-extensions).
- [7-Zip](https://www.7-zip.org/)
  - ?7-Zip Theme Manager
- [Adobe GenP](https://www.reddit.com/r/GenP/)
- [BetterDiscord](https://github.com/BetterDiscord/BetterDiscord)
  - Use `pnpm` and build from source instead of using their installer.
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
  - `winget install Docker.DockerDesktop`
- [PowerToys](https://apps.microsoft.com/store/detail/XP89DCGQ3K6VLD)
  - `winget install powertoys`
- [VLC](https://www.videolan.org/vlc/)
-  [SecureUxTheme](https://github.com/namazso/SecureUxTheme)
  - To get themes working. 
- ?[EarTrumpet](https://apps.microsoft.com/store/detail/9NBLGGH516XP)
  - `winget install eartrumpet`
- ?$[Nilesoft Shell](https://nilesoft.org/)
- ?[FileZilla](https://filezilla-project.org/)
- ?[qBittorrent](https://www.qbittorrent.org/)
- ?$[VBCable](https://vb-audio.com/Cable/)
  - Alternatives:
    - [soundsync](https://github.com/geekuillaume/soundsync)

## BROWSER EXTENSIONS

Chrome and all it's derivatives are garbage, use Firefox.   

- [Bitwarden](https://bitwarden.com/)  
- [ClearURLs](https://github.com/ClearURLs/Addon/)  
- [Dark Reader](https://darkreader.org/)
  - Alternatives:
    - [Stylus](https://addons.mozilla.org/addon/styl-us/)
    - [Midnight Lizard](https://addons.mozilla.org/addon/midnight-lizard-quantum/) 
- [Demodal](https://github.com/AliasIO/demodal)  
- [uBlock Origin](https://ublockorigin.com/)  
- [DDG Privacy Essentials](https://addons.mozilla.org/addon/duckduckgo-for-firefox/)  
- [FastForward](https://github.com/FastForwardTeam/FastForward)  
- [Firefox Color](https://color.firefox.com/)
- [Lighthouse](https://github.com/GoogleChrome/lighthouse)  
- [External Application Launcher](https://addons.mozilla.org/en-US/firefox/addon/external-application/) 
  - Use with `yt-dlp` for downloading videos.  
- [Privacy Badger](https://privacybadger.org/)  
- [Redirect AMP to HTML](https://addons.mozilla.org/en-US/firefox/addon/amp2html/)  
- [Return Youtube Dislike](https://www.returnyoutubedislike.com/)  
- [Search by Image](https://addons.mozilla.org/en-US/firefox/addon/search_by_image/)  
- [Sponsorblock](https://github.com/ajayyy/SponsorBlock)  
- ?[VisBug](https://github.com/GoogleChromeLabs/ProjectVisBug)  
- ?[Disable Page Visibility API](https://addons.mozilla.org/en-US/firefox/addon/disable-page-visibility/)  

## DISCORD

### PLUGINS
- [BetterVolume](https://betterdiscord.app/plugin/BetterVolume)
- [BetterRoleColors](https://betterdiscord.app/plugin/BetterRoleColors)
- [CallTimeCounter](https://betterdiscord.app/plugin/CallTimeCounter)
- [CharCounter](https://betterdiscord.app/plugin/CharCounter)
- [DoubleClickToEdit](https://betterdiscord.app/plugin/Double%20Click%20To%20Edit)
- [ImageUtilities](https://betterdiscord.app/plugin/ImageUtilities)
- [SpotifyControls](https://betterdiscord.app/plugin/SpotifyControls)
- [QuickLastMessage](https://betterdiscord.app/plugin/QuickLastMessage)

### THEMES
- [GT-RevertRebrand](https://github.com/Goose-Nest/GT-RevertRebrand)
- [revert.theme.css](https://gist.github.com/styxpilled/727554b063dd2b0fee5db7e47138e231)

## MINECRAFT

You probably want an alternative launcher. [Prism Launcher](https://github.com/PrismLauncher/PrismLauncher) is open source.  
Use [Fabric](https://fabricmc.net/) or alternatively [Quilt](https://quiltmc.org/en/about/faq/) which is a hard fork of Fabric. 

### GLOSSARY
- [Modrinth](modrinth.com/) is a open-source mod platform.
  
### BACKEND
- [FabricApi](https://modrinth.com/mod/fabric-api)
  - Essential for using most Fabric mods.
- [Quilted Fabric API](https://modrinth.com/mod/qsl)
  - Essential for using Quilt || Fabric mods on Quilt.
- [ModMenu](https://modrinth.com/mod/modmenu)
  - Adds a mod menu.
- [Cloth Config API](https://modrinth.com/mod/cloth-config)
  - Config screen api.
- [MaLiLib](https://www.curseforge.com/minecraft/mc-mods/malilib)
  - Required by Litematica, MiniHUD and Tweakeroo.
- ?[CIT Resewn](https://modrinth.com/mod/cit-resewn)
  - Custom Item Textures. Required by some resource packs.

### PERFORMANCE
- [Sodium](https://modrinth.com/mod/sodium)
  - Non-destructive rendering optimization.
- [Indium](https://modrinth.com/mod/indium)
  - Provides Fabric Rendering API support for Sodium.
- [Reese's Sodium Options](https://modrinth.com/mod/reeses-sodium-options)
  - Alternative options menu for Sodium.
- [Lithium](https://modrinth.com/mod/lithium)
  - General purpose optimization.
- [Phosphor](https://modrinth.com/mod/phosphor)
  - Non-destructive lighting engine optimization.
- [LazyDFU](https://modrinth.com/mod/lazydfu)
  - Makes the game boot faster by deferring non-essential initialization.
- [EntityCulling](https://modrinth.com/mod/entityculling)
  - Using async path-tracing to skip rendering blocks / entities that are not visible.
- [FerriteCore](https://modrinth.com/mod/ferrite-core)
  - Memory usage optimizations.
- [Dynamic FPS](https://modrinth.com/mod/dynamic-fps)
  - Reduce framerate || disable rendering when Minecraft isn't focused.
- [Cull Less Leaves](https://modrinth.com/mod/cull-less-leaves)
  - Customizable leaf culling. Improved version of [Cull Leaves](https://modrinth.com/mod/cull-leaves).
- [Language Reload](https://modrinth.com/mod/language-reload)
  - Speeds up language change load times.
- [BetterBeds](https://modrinth.com/mod/better-beds)
  - Removes the block entity renderer from the bed and replaces it with the default minecraft model renderer. 

### RENDERING
- [Iris](https://modrinth.com/mod/iris)
  - Shaders.
- [Continuity](https://modrinth.com/mod/continuity)
  - Efficient connected textures.
- [LambDynamicLights](https://modrinth.com/mod/lambdynamiclights)
  - Dynamic lights.
- [LambdaBetterGrass](https://modrinth.com/mod/lambdabettergrass)
  - Grass eyecandy.
- [Bobby](https://modrinth.com/mod/bobby)
  - Allows for render distances greater than the server's view-distance by caching chunks.
- [Distant Horizons](https://modrinth.com/mod/distanthorizons)
  - LOD for chunks.
- [MiniHUD](https://www.curseforge.com/minecraft/mc-mods/minihud)
  - Various overlays.
- [LightLevel](https://www.curseforge.com/minecraft/mc-mods/lightlevel)
  - Show light levels.
- [Light Overlay](https://modrinth.com/mod/light-overlay)
  - Show light levels.
- [Falling Leaves](https://modrinth.com/mod/fallingleaves)
  - Falling leaf particle effects.
- [ClearDespawn](https://modrinth.com/mod/cleardespawn)
  - Make items blink when they're about to despawn.
- [Better Biome Blend](https://modrinth.com/mod/better-biome-blend)
  - Improves the look and performance of biome color transitions.
- [3D Skin Layers](https://modrinth.com/mod/3dskinlayers)
  - Replaces the 2d second layer of player skins with a 3d modeled version. Will automatically switch to the vanilla 2d rendering when players are further away than 12 blocks

### UI
- $[Inventory HUD+](https://www.curseforge.com/minecraft/mc-mods/inventory-hud-forge)
  - Improved inventory HUD.
- [AppleSkin](https://modrinth.com/mod/appleskin)
  - Food || hunger related HUD improvements.
- [Better Mount HUD](https://modrinth.com/mod/better-mount-hud)
  - Improved mounted HUD.
- [Roughly Enough Items](https://modrinth.com/mod/roughly-enough-items)
  - Search through items.
- [MoreChatHistory](https://modrinth.com/mod/morechathistory)
  - Increases the maximum length of chat history from 100 to 16384.
- [Compact Chat](https://modrinth.com/mod/compact-chat)
  - Merge duplicate chat messages.
- [ShulkerBoxTooltip](https://modrinth.com/mod/shulkerboxtooltip)
  - View the contents of shulker boxes from your inventory.
- [Inventory Tabs](https://modrinth.com/mod/inventory-tabs-updated)
  - Access nearby blocks without leaving your inventory.
- [BoatHud](https://modrinth.com/mod/boathud)
  - Improved boat HUD.
- [Status Effect Bars](https://modrinth.com/mod/status-effect-bars)
  - Shows a progress bar on status effects.
- [Dark Loading Screen](https://modrinth.com/mod/dark-loading-screen)
  - Makes the loading screen darker.
- [ToolTipFix](https://modrinth.com/mod/tooltipfix)
  - Stops tooltips from overflowing the screen.
- [ItemSwapper](https://modrinth.com/plugin/itemswapper)
  - Item hotswapping.

### MISC
- [Sodium Extra](https://modrinth.com/mod/sodium-extra)
  - Provides some OptiFine's features to Sodium.
- [BetterF3](https://modrinth.com/mod/betterf3)
  - Replaces the F3 menu with a customizable, more human-readable HUD.
- [AntiGhost](https://modrinth.com/mod/antighost)
  - Removes ghost blocks by requesting resends from the server.
- [Borderless Mining](https://modrinth.com/mod/borderless-mining)
  - Changes fullscreen to use a borderless window.
- ?[Tweakeroo](https://www.curseforge.com/minecraft/mc-mods/tweakeroo)
  - A bundle of various tweaks.
- [Freecam](https://www.curseforge.com/minecraft/mc-mods/free-cam)
  - Control your camera separately from the player. The Modrinth version doesn't allow noclip.
- [ChestTracker](https://modrinth.com/mod/chest-tracker)
  - Highlight blocks where you've put your items.
- [Double Doors](https://modrinth.com/mod/double-doors)
  - Open || close double doors with one click.
- [Eating Animation](https://modrinth.com/mod/eating-animation)
  - Nicer eating animation.

### BUILDING
- [Litematica](https://www.curseforge.com/minecraft/mc-mods/litematica)
  - Show various schematics as an overlay.
- [Litematica Printer](https://modrinth.com/mod/litematica-printer)
  - Automatically build Litematica structures.
- [Litermatica Server Paster](https://modrinth.com/mod/litematica-server-paster)
  - Paste Litematica structures. Needs to be installed both on the client and server.
- [World Edit](https://www.curseforge.com/minecraft/mc-mods/worldedit)
  - In-game map editor. Works only on singleplayer. 

### RESOURCE PACKS
  - $[VanillaTweaks](https://vanillatweaks.net/picker/resource-packs/)
    - Various tweaks.
  - [Default Dark Mode](https://modrinth.com/resourcepack/default-dark-mode)
    - Gives the Minecraft GUI dark mode while maintaining the vanilla textures.
  - [xali's Enhanced Vanilla](https://modrinth.com/resourcepack/xalis-enhanced-vanilla)
    - Makes a few blocks look nicer without changing the overall feel.
  - ?[Even Better Enchants](https://modrinth.com/resourcepack/even-better-enchants)
    - Unique textures for all enchanted books. Requires [Cit Resewn](https://modrinth.com/mod/cit-resewn).

### SHADERS
  - [Rethinking Voxels](https://modrinth.com/shader/rethinking-voxels)

### DEVELOPMENT
- [Fabric Language Kotlin](https://modrinth.com/mod/fabric-language-kotlin)
  - Use a language that isn't bad to [make mods](https://github.com/FabricMC/fabric-language-kotlin#usage).