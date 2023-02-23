This is a list containing all of the instructions to more-or-less replicate my setup as of 02.2023.  
I'll update this with links and explanations in the future.

1. [SHELL](#shell)
2. [PROGRAMS](#programs)
3. [BROWSER EXTENSIONS](#browser-extensions)
4. [DISCORD](#discord)
5. [BLENDER](#blender)
   1. [ADDONS](#addons)
   2. [ASSETS](#assets)

## GLOSSARY

- You should probably install them in the order you see them.
- `?` prefix means I either don't like this option and suggest finding an alternative in the future, or see this as something optional in general.  
- `M$` suffix means this is something you can install via `winget` or the Microsoft Store.

## SHELL

Windows Terminal  
ForceBindIP  
curl  
git  
gsudo  
ImageMagick  
NVM  
pyenv  
Oh My Posh  
fzf  
yt-dlp  

## PROGRAMS

- [Firefox](https://www.mozilla.org/en-US/firefox/new/)
  - Notes:
    - `Chromium` has problems and doesn't work as well as Chrome.
    - Never use or install Brave.
    - Refer to the [extensions section](#browser-extensions).
- [7-Zip](https://www.7-zip.org/)  
  - Extra:
    - 7-Zip Theme Manager
- [Adobe GenP](https://www.reddit.com/r/GenP/)
- [BetterDiscord](https://github.com/BetterDiscord/BetterDiscord)  
  - Notes:
    - Use `pnpm` and build from source instead of using their installer.  
- [EarTrumpet M$](https://apps.microsoft.com/store/detail/9NBLGGH516XP)
  - Winget:
    - `winget install eartrumpet`
- [PowerToys M$](https://apps.microsoft.com/store/detail/XP89DCGQ3K6VLD)
  - Winget:
    - `winget install powertoys`
- [VLC](https://www.videolan.org/vlc/)  
  - Notes:
    - This is messy.
    - Sometimes the video plays in a window called `DirectX 3D`. This usually takes a few hours to solve and I don't really know what solves this.
    - Newer versions might be even more broken.
    - Version `2.2.8 Weatherwax` seems to work fine.
  - Alternatives:
    - [mpv](https://mpv.io/)
    - [mpv.net](https://github.com/mpvnet-player/mpv.net)
- UXThemePatcher  
  - Notes:
    - This is weird, unsafe, closed-source software.  
  - Alternatives:
    - [SecureUxTheme](https://github.com/namazso/SecureUxTheme) 
- [Nilesoft Shell](https://nilesoft.org/)
- ?[Auto Hot Key](https://www.autohotkey.com/)? 
  - Alternatives:
    - Use Python. This is exactly the sort of stuff Python was made for. Use libaries like `pynput` and `tkinter`. A glorified scripting language is better than a literal scripting language that can't do anything past simulating some keypresses.
- ?[Bulk Rename Utility](https://www.bulkrenameutility.co.uk/)  
  - Alternatives:
    - Just write a short script to do it for you.
- ?[FileZilla](https://filezilla-project.org/)  
- ?[spicetify](https://github.com/spicetify/spicetify-cli)  
  - Notes
    - Very unstable most of the time.
- ?[qBittorrent](https://www.qbittorrent.org/)  
- ?[VBCable](https://vb-audio.com/Cable/)  
  - Alternatives:
    - [soundsync](https://github.com/geekuillaume/soundsync)

## BROWSER EXTENSIONS

[Bitwarden](https://bitwarden.com/)  
[ClearURLs](https://github.com/ClearURLs/Addon/)  
?Dark Reader || stylus || Midnight Lizard  
[Demodal](https://github.com/AliasIO/demodal)  
?[Disable Page Visibility API](https://addons.mozilla.org/en-US/firefox/addon/disable-page-visibility/)  
[DDG Privacy Essentials](https://addons.mozilla.org/en-US/firefox/addon/duckduckgo-for-firefox/)  
[FastForward](https://github.com/FastForwardTeam/FastForward)  
[Firefox Color](https://color.firefox.com/)
[Lighthouse](https://github.com/GoogleChrome/lighthouse)  
Open With (use with yt-dlp for downloading videos)  
[Privacy Badger](https://privacybadger.org/)  
[Redirect AMP to HTML](https://addons.mozilla.org/en-US/firefox/addon/amp2html/)  
[Return Youtube Dislike](https://www.returnyoutubedislike.com/)  
[Search by Image](https://addons.mozilla.org/en-US/firefox/addon/search_by_image/)  
[Sponsorblock](https://github.com/ajayyy/SponsorBlock)  
?Tranquility Reader || Reader View  
[uBlock Origin](https://ublockorigin.com/)  
?Urban VPN  
[Wikiwand](https://www.wikiwand.com/)  
[VisBug](https://github.com/GoogleChromeLabs/ProjectVisBug)  
?Material Color Palette  
WhatFont  

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

## BLENDER

### ADDONS

Node Wrangler (builtin)

### ASSETS

[800 Procedural Materials](https://adamantitemachine.com/b3dmatpack/)
