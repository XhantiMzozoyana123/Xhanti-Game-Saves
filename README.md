# D-Drive-GameSaves

A single git repository containing backups of all game save files from this PC,
organized per game. Originals were **copied** (not moved), so the games still
read from their normal locations.

## Contents & original source locations

| Folder in this repo | Original location on disk |
|---|---|
| `Cyberpunk 2077/Saved Games/Cyberpunk 2077` | `C:\Users\Shadow\Saved Games\CD Projekt Red\Cyberpunk 2077` |
| `Cyberpunk 2077/AppData/Cyberpunk 2077` | `C:\Users\Shadow\AppData\Local\CD Projekt Red\Cyberpunk 2077` (settings) |
| `ELDEN RING/Roaming/EldenRing` | `C:\Users\Shadow\AppData\Roaming\EldenRing` |
| `Marvel's Spider-Man 2/Documents/Marvel's Spider-Man 2` | `C:\Users\Shadow\Documents\Marvel's Spider-Man 2` |
| `Marvel's Spider-Man 2/Roaming/Insomniac Games` | `C:\Users\Shadow\AppData\Roaming\Insomniac Games` (settings/crash data) |
| `Marvel's Spider-Man 2/unlock_psn_bonuses` | `D:\Games\Marvel's Spider-Man 2\unlock_psn_bonuses` |
| `Need For Speed Unbound/Documents/SaveGame` | `C:\Users\Shadow\Documents\Need For Speed(TM) Unbound\SaveGame` |
| `Need For Speed Unbound/Documents/settings` | `C:\Users\Shadow\Documents\Need For Speed(TM) Unbound\settings` |
| `DOOM The Dark Ages/Saved Games/id Software` | `C:\Users\Shadow\Saved Games\id Software` |
| `Dragon Ball Z - Kakarot/Steam RUNE 851850` | `C:\Users\Public\Documents\Steam\RUNE\851850` (autosave/manual/system saves + achievements) |
| `Dragon Ball Z - Kakarot/AppData AT/Saved/Config` | `C:\Users\Shadow\AppData\Local\AT\Saved\Config` (game settings) |
| `Steam Emulator/Goldberg SteamEmu Saves` | `C:\Users\Shadow\AppData\Roaming\Goldberg SteamEmu Saves` |
| `Steam Emulator/GSE Saves` | `C:\Users\Shadow\AppData\Roaming\GSE Saves` |

## Restoring a save

Copy the files from the repo folder back to the original location listed above,
overwriting the existing files, with the game closed.

## Updating the backup

After playing, re-copy the changed save folders into this repo and commit:

```powershell
# example: refresh Elden Ring save
Copy-Item 'C:\Users\Shadow\AppData\Roaming\EldenRing\*' `
  'D:\Games\D-Drive-GameSaves\ELDEN RING\Roaming\EldenRing\' -Recurse -Force
git add -A; git commit -m "Update Elden Ring save"
```
