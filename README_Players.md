# VoidSteam

**Play FNAF Online Multiplayer with your friends over Steam, without needing Unity's online services.**

VoidSteam is a mod for *FNAF Online Multiplayer 0.9.6-alpha*. It connects players through Steam's relay network and adds its own voice chat. You still host and join from the game's normal menus.

> Unofficial community mod by **voidcrew**. Not affiliated with the game's developers, Unity or Valve.

---

## Features

- **Play through Steam.** All game traffic and voice go through Steam's relay servers. Players connect through Steam and never see each other's IP addresses.
- **Room codes.** The host gets a short 6-character code to send to friends.
- **Public or private rooms.** Public rooms appear in the *Play Online* list for other VoidSteam players. Private rooms can only be joined with the code.
- **Voice chat built in.** Speaking icons, mute lists, volume sliders and the phone call all work. The Purple Guy can still eavesdrop.
- **Microphone picker.** *Settings > MIC SETUP* works again.
- **Up to 5 players** in a room: the host plus 4 friends.

---

## What you need

Every player needs all of these:

- **FNAF Online Multiplayer 0.9.6-alpha**
- **MelonLoader 0.7.3** installed into the game
- **Steam** open and signed in
- These files in the game folder:

| File | Where it goes |
|---|---|
| `VoidSteam.dll` | `<game folder>\Mods` |
| `Steamworks.NET.dll` | `<game folder>\UserLibs` |
| `steam_api64.dll` | next to the game's `.exe` |

Everyone in a room must be on the **same game version**. If yours is different, the host turns you away and the game tells you why.

---

## Installing

1. Install **MelonLoader 0.7.3** into the game, then start the game once and close it.
2. Copy the three files from the table above into their folders.
3. Open Steam and sign in.
4. Start the game. A short **"LOADING VOIDSTEAM"** bar at the bottom of the screen means the mod is running.

---

## How to play

### Host a game
Press the game's normal **Create Lobby** button. VoidSteam creates the room and gives you a 6-character code. Send the code to your friends.

### Join a game
Type the host's code into the game's code box and press **JOIN**. You can also pick a public room from the **Play Online** list.

> Codes never use `0`, `O`, `1` or `I`, so look-alike characters can't be mixed up.

### Controls

| Key | What it does |
|---|---|
| `F6` | Mute or unmute your microphone |
| `F7` (or click the box in the top-left corner) | Switch between the game's original voice chat (Vivox) and VoidSteam voice. The box only shows in the menus and lobby, and only when Vivox is available. |
| *Settings > MIC SETUP* | Choose your microphone. Your choice is saved. |

---

## How it connects

1. When you host, VoidSteam posts your room on Steam's lobby list with its code. Nobody plays inside that lobby. It only tells other players how to find you.
2. When a friend enters the code, Steam finds your room and connects them to you through **Steam's relay servers**.
3. All game data and voice travel over that Steam connection. Direct connections are switched off, so your IP address is never shared with other players.

---

## Things you might notice

- **Steam shows "Spacewar" as your game.** VoidSteam uses Steam's free test app to connect, so Steam displays that name while you play. This is normal.
- **A `steam_appid.txt` file appears in the game folder.** VoidSteam creates it so Steam works even if you don't launch the game through Steam. Leave it there.
- **The mod never changes the game's files on disk.** Removing `VoidSteam.dll` from `Mods` returns the game to normal.

---

## Settings (optional)

Most players never need to change anything. If you want to, close the game and open `<game folder>\UserData\MelonPreferences.cfg`. The settings are under `[VoidTalk]`.

| Setting | Default | What it does |
|---|---|---|
| `VoiceThreshold` | `700` | How loud you must be before your mic sends. Raise it if background noise keeps getting through, lower it if you get cut off. |
| `VoiceVolume` | `1.0` | How loud other players sound |
| `VoiceChat` | `true` | Set to `false` to turn off VoidSteam voice chat |
| `LoadingBar` | `true` | Set to `false` to hide the loading bar |

---

## Troubleshooting

| Problem | Try this |
|---|---|
| "Steam is not running" | Open Steam, sign in, then restart the game. |
| "steam_api64.dll is missing" | Put the **64-bit** `steam_api64.dll` next to the game's `.exe`. |
| No loading bar, nothing happens | Check that MelonLoader 0.7.3 is installed and `VoidSteam.dll` is in `Mods`. |
| Friend can't join | Make sure you're both on the same game version, the code is typed correctly, and the room isn't full (5 players max). |
| Can't host or join after a game update | The mod may not support the new version yet. Hosting and joining stay off on purpose until it's updated. |
| Nobody can hear me | Check *Settings > MIC SETUP*, make sure you're not muted (`F6`), and try lowering `VoiceThreshold`. |
| Voice chat stopped working after a crash | VoidSteam switches voice to a safer mode after a crash. Restart the game. If it keeps happening, report it. |

If you report a problem, include `<game folder>\MelonLoader\Latest.log`. It shows what the mod did at startup.

---

## Credits

Made by **voidcrew**. Runs on [MelonLoader](https://github.com/LavaGang/MelonLoader) and [Steamworks.NET](https://github.com/rlabrecque/Steamworks.NET).
