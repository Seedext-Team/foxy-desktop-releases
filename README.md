# Foxy releases

Public downloads for [Foxy](https://seedext.com), Seedext's live transcription
app, and the feed its self-updater polls.

## Download

These links always point to the newest stable release:

- **macOS** (Apple Silicon, macOS 14.4 or later):
  [Foxy_aarch64.dmg](https://github.com/Seedext-Team/foxy-desktop-releases/releases/latest/download/Foxy_aarch64.dmg).
  Open the DMG and drag Foxy to Applications.
- **Windows** (x64):
  [Foxy_x64-setup.exe](https://github.com/Seedext-Team/foxy-desktop-releases/releases/latest/download/Foxy_x64-setup.exe)
- **Windows** (ARM64):
  [Foxy_arm64-setup.exe](https://github.com/Seedext-Team/foxy-desktop-releases/releases/latest/download/Foxy_arm64-setup.exe)

The Windows installer is not signed with a code-signing certificate yet, so
SmartScreen calls the publisher unknown. Click **More info**, then
**Run anyway**.

If a link does not work, download the same files from the
[newest release's page](https://github.com/Seedext-Team/foxy-desktop-releases/releases/latest).
Once installed, Foxy updates itself.

`CHANGELOG.md` lists what changed in each stable version.

## For the updater

`latest.json` on the newest release is the stable channel's manifest, and
`channels/rc/latest.json` is the release-candidate channel's. No code lives
here: this repository exists so that shipped apps can fetch updates without
credentials.
