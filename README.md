# VoidLinx

**Play FNAF Online Multiplayer with your friends over Steam, without needing Unity's online services.**

VoidLinx 1.1.0 is a mod for *FNAF Online Multiplayer 0.9.6-alpha*. It connects players through Steam's relay network and adds its own voice chat. You still host and join from the game's normal menus.

> Unofficial community mod by **voidcrew**. Not affiliated with the game's developers, Unity or Valve.

---

## Features

- **Play through Steam.** All game traffic and voice go through Steam's relay servers. Players connect through Steam and never see each other's IP addresses.
- **Room codes.** The host gets a short 6-character code to send to friends.
- **Public or private rooms.** Public rooms appear in the *Play Online* list for other VoidLinx players. Private rooms can only be joined with the code.
- **Voice chat built in.** Speaking icons, mute lists, volume sliders and the phone call all work. The Purple Guy can still eavesdrop.
- **Microphone picker.** *Settings > MIC SETUP* works again.
- **Up to 5 players** in a room: the host plus 4 friends.

---

## What you need

Every player needs all of these:

- **FNAF Online Multiplayer 0.9.6-alpha**
- **MelonLoader 0.7.3** installed into the game
- **Steam** open and signed in
- These files in the game folder (the setup or the zip from **Installing** below puts them there for you):

| File | Where it goes |
|---|---|
| `VoidLinx.dll` | `<game folder>\Mods` |
| `Steamworks.NET.dll` | `<game folder>\UserLibs` |
| `steam_api64.dll` | next to the game's `.exe` |

Everyone in a room must be on the **same game version**. If yours is different, the host turns you away and the game tells you why.

---

## Installing

1. Install **MelonLoader 0.7.3** into the game, then start the game once and close it.
2. Put the VoidLinx files in the game folder. Pick one of these two ways:
   - **Run the setup.** Download `VoidLinx-1.1.0-Setup.exe` and double-click it. If it isn't inside the game folder, it asks you to pick the game's `.exe`. It puts the three files in the right folders and removes old `VoidSteam.dll` and `VoidTalk.dll` files from `Mods`, which clash with VoidLinx.
   - **Extract the zip yourself.** Download `VoidLinx-1.1.0.zip` and extract it into the game folder, the one that holds `FNAF Online Multiplayer.exe`. The files land in the folders from the table above. Delete any old `VoidSteam.dll` or `VoidTalk.dll` from `Mods`. Copying the three files by hand works the same way.
3. Open Steam and sign in.
4. Start the game. A short **"LOADING VOIDLINX"** bar at the bottom of the screen means the mod is running.

> Windows may say **"Windows protected your PC"** when you start the setup, because the file isn't code-signed. Click **More info**, then **Run anyway**. If you'd rather not, use the zip.

---

## How to play

### Host a game
Press the game's normal **Create Lobby** button. VoidLinx creates the room and gives you a 6-character code. Send the code to your friends.

### Join a game
Type the host's code into the game's code box and press **JOIN**. You can also pick a public room from the **Play Online** list.

> Codes never use `0`, `O`, `1` or `I`, so look-alike characters can't be mixed up.

### Controls

| Key | What it does |
|---|---|
| *Settings > MIC SETUP* | Choose your microphone. Your choice is saved. |

---

## How it connects

1. When you host, VoidLinx posts your room on Steam's lobby list with its code. Nobody plays inside that lobby. It only tells other players how to find you.
2. When a friend enters the code, Steam finds your room and connects them to you through **Steam's relay servers**.
3. All game data and voice travel over that Steam connection. Direct connections are switched off, so your IP address is never shared with other players.

---

## Things you might notice

- **Steam shows "Spacewar" as your game.** VoidLinx uses Steam's free test app to connect, so Steam displays that name while you play. This is normal.
- **A `steam_appid.txt` file appears in the game folder.** VoidLinx creates it so Steam works even if you don't launch the game through Steam. Leave it there.
- **The mod never changes the game's files on disk.** Removing `VoidLinx.dll` from `Mods` returns the game to normal.

---

## Settings (optional)

Most players never need to change anything. If you want to, close the game and open `<game folder>\UserData\MelonPreferences.cfg`. The settings are under `[VoidTalk]`.

| Setting | Default | What it does |
|---|---|---|
| `VoiceThreshold` | `700` | How loud you must be before your mic sends. Raise it if background noise keeps getting through, lower it if you get cut off. |
| `VoiceVolume` | `1.0` | How loud other players sound |
| `VoiceChat` | `true` | Set to `false` to turn off VoidLinx voice chat |
| `LoadingBar` | `true` | Set to `false` to hide the loading bar |

---

## Troubleshooting

| Problem | Try this |
|---|---|
| "Steam is not running" | Open Steam, sign in, then restart the game. |
| "Steam is not running" | Check if one is setup with administrator, then make sure the other is running with or without it as well |
| "steam_api64.dll is missing" | Put the **64-bit** `steam_api64.dll` next to the game's `.exe`. |
| No loading bar, nothing happens | Check that MelonLoader 0.7.3 is installed and `VoidLinx.dll` is in `Mods`. |
| Friend can't join | Make sure you're both on the same game version, the code is typed correctly, and the room isn't full (5 players max). |
| Can't host or join after a game update | The mod may not support the new version yet. Hosting and joining stay off on purpose until it's updated. |
| Nobody can hear me | Check *Settings > MIC SETUP*, make sure you're not muted, and try lowering `VoiceThreshold`. |
| Voice chat stopped working after a crash | VoidLinx switches voice to a safer mode after a crash. Restart the game. If it keeps happening, report it. |

If you report a problem, include `<game folder>\MelonLoader\Latest.log`. It shows what the mod did at startup.

---

## Credits

Made by **voidcrew**. Runs on [MelonLoader](https://github.com/LavaGang/MelonLoader) and [Steamworks.NET](https://github.com/rlabrecque/Steamworks.NET).
