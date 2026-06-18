# HexWar Builds

Distribution repo for **HexWar Remake** packaged Windows builds. The game's
auto-updating launcher reads this repo's **Releases** to keep every player on the
same build.

> This repo holds **only release zips** — not the game source or project (that's
> ~27 GB and lives elsewhere). Build zips ride in as **release assets**, which are
> stored off-repo and need no Git LFS.

## Publishing a new build

1. Repackage the game (UE: `BuildCookRun … -archivedirectory=…\Packaged`).
2. Zip the **contents** of `Packaged\Windows\` so `HexWarRemake.exe` is at the zip
   root. Name it `HexWarRemake-Windows-vX.Y.Z.zip`.
3. Create a **Release** here tagged `vX.Y.Z` (bump every time — the launcher
   compares tags), attach the zip, and publish.

Every launcher picks it up on next start. Build host must stay **public** for the
launcher's tokenless reads.
