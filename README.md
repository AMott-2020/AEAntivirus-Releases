# AEAntivirus Releases

Public download host for the AEAntivirus installer and update binaries.

The AEAntivirus source code lives in a private repository. The files in
this repo are only the compiled binaries that AEAntivirus clients and
the aeantivirus.com download page fetch:

- `AEAntivirus-Setup.exe` — Windows installer (32-bit)
- `AEAntivirus-Setup-x64.exe` — Windows installer (64-bit)
- `AEAntivirus-Setup.patch` / `AEAntivirus-Setup-x64.patch` — delta
  update patches for the Windows client updater
- `aeantivirus.apk` — Android app
- `aeantivirus-linux.tar.gz` — Linux daemon package
- `aeantivirus-macos.tar.gz` — macOS daemon package

Every download is verified by the client against the SHA-256 hash in
the update manifest served by aeantivirus.com before it is installed,
so a file that does not match its manifest is refused automatically.

Published by `server/scripts/publish-binaries-github.sh` in the private
AEAntivirus repo (called at the end of `build.sh` and
`publish-update.sh`). Do not edit or replace these files by hand.
