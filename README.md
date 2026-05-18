## Preview syncing if i delete the local saves
https://github.com/user-attachments/assets/faf972f2-163b-46fd-bf62-3d66ebc43e0d

## Denuvo Authorization without ETicket and AppTicket
https://github.com/user-attachments/assets/5ca3c0bc-9c07-405e-953b-f021a8d32ab0

## Achievement Works on Game that is not popular
https://github.com/user-attachments/assets/30c89470-5bc3-4092-abda-e6dc7136f1ac


## Feature

### Core Unlocks
- Unlock an unlimited number of unowned games.
- Unlock all DLCs for unowned games.
- Support auto load depot decryption keys from Lua config, no need to manually input them in `config.vdf` anymore.
- Support auto manifest download via `steamrun` / `wudrm` upstream APIs, or a custom Lua endpoint (see [Manifest via Lua](#manifest-via-lua)).
- Support downloading protected games or DLCs that require an access token.
- Support binding manifest to prevent specific games from being updated, it will be writen to `appinfo.vdf` so if you don't want to bind anymore, just delete the corresponding entry in `appinfo.vdf` and delete this bind from Lua.
- Using the 480 AppID network spoof for Online-Fix
- Patch All SteamStub Variant.
- Fix error game launch error code 86 & 54 for UE Games
- Spoof playing status of what you playing
  
### Family Sharing and Remote Play
- Bypass Steam Family Sharing restrictions, allowing shared games to be played without limitations.

### Compatible with games protected by Denuvo and SteamStub
- Denuvo Authorization by just playing once on owned account.
- For games protected by Denuvo and SteamStub, find a safe timing to switch `GetSteamID` (see `src/Hook/Hooks_IPC.cpp#Handler_IClientUser_GetSteamID`) so save files are not affected. (Completed)

### Stats and Achievements
- Fully working Stats and Achievements
- Now it will fetch using setstat from the default steamid if its fails then fallback to the local implemented achievement system

### Steam Cloud using Cloud Redirect Integration
- Full Steam Cloud synchronization support. (Completed)

### TO-DO
- None

## Disclaimer
This project is provided for research and educational purposes only. You are responsible for complying with local laws, platform terms of service, and software licenses.
