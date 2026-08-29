# weeboop [![Tests](https://github.com/PrantoSMSS/weeboop/actions/workflows/ci.yml/badge.svg)](https://github.com/PrantoSMSS/weeboop/actions/workflows/ci.yml) [![Excavator](https://github.com/PrantoSMSS/weeboop/actions/workflows/excavator.yml/badge.svg)](https://github.com/PrantoSMSS/weeboop/actions/workflows/excavator.yml)

A [Scoop](https://scoop.sh) bucket focused on accumulating all the weeb and otaku based applications. It is a fork of [Rinkerbel/scooped](https://github.com/Rinkerbel/scooped).

## List of applications in this bucket

> Click here to [browse the list on scoop instead](https://scoop.sh/#/apps?q="https://github.com/PrantoSMSS/weeboop"&o=false)

### Anime & Manga

- [Seanime](https://github.com/5rahim/seanime)
- [Shiru](https://github.com/RockinChaos/Shiru)
- [Hayase](https://github.com/hayase-app/ui) [^1]
- [zenshin](https://github.com/hitarth-gg/zenshin)
- [Totoro](https://github.com/insomniachi/Totoro)
- [AnymeX](https://github.com/RyanYuuki/AnymeX)
- [Toru](https://github.com/sweetbbak/toru)
- [GoAnime](https://github.com/alvarorichard/GoAnime)
- [Mangayomi](https://github.com/kodjodevf/mangayomi)
- [MangaJaNaiConverterGui](https://github.com/the-database/MangaJaNaiConverterGui)
- [SyncYomi](https://github.com/syncyomi/syncyomi)
- [ShokoServer](https://github.com/ShokoAnime/ShokoServer)
- [Unyo](https://github.com/K3vinb5/unyo-app)
- [Suwayomi-VaadinUI](https://github.com/Suwayomi/Suwayomi-VaadinUI) [^2]

### Visual Novel & Text Hooking

- [Textractor](https://github.com/Artikash/Textractor) [^3]

### Language & Dictionaries

- [meikipop](https://github.com/rtr46/meikipop) [^4]

### Voice & Music Synthesis

- [Vogen](https://github.com/aqtq314/Vogen.Client)
- [Audacity (legacy 2.4.1)](https://www.audacityteam.org)

### Downloaders & Automation

- [autobrr](https://github.com/autobrr/autobrr)
- [qui](https://github.com/autobrr/qui)

### Utilities & Misc

- [Twitch-Channel-Points-Miner](https://github.com/rdavydov/Twitch-Channel-Points-Miner-v2) [^5]
- [shelter-installer](https://github.com/uwu/shelter-installer)
- [SteamTokenDumper](https://github.com/SteamDatabase/SteamTokenDumper)
- [ShareX-HDR](https://github.com/GotoFinal/ShareX-HDR)
- [LuaTools](https://lua.tools) [^6]

[^1]: Previously known as Miru
[^2]: Requires a Java Runtime Environment 21 or newer (JRE 21+) installed on the system to run.
[^3]: Some antivirus engines flag the installer's temp file as a false-positive trojan. This is a known false positive caused by Textractor's core function: injecting into game processes to hook text output.
[^4]: Runs from the system tray. Right-click the tray icon to open settings, reselect the scan region, or change the OCR provider.
[^5]: Requires Python. After installing, navigate to the app directory (`scoop prefix TwitchChannelPointsMiner`) and run `pip install -r requirements.txt`, then configure `run.py` before running.
[^6]: Requires the .NET 8 Desktop Runtime to run.

## Usage

After installing [Scoop](https://scoop.sh/), enter the following line in a
Command Prompt or PowerShell window:

```powershell
scoop bucket add weeboop https://github.com/PrantoSMSS/weeboop
```

Once this is done, you can install any app from this bucket.\
For instance, use the following command:

```powershell
scoop install unyo
```
