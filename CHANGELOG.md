# Changelog

What changed in Foxy, newest first.

## 0.2.0 (2026-08-11)

### Features

- Foxy updates itself. When a newer version is out, an Update button appears in the drawer; Foxy downloads it and comes back on the new version only when you press Restart.
- Settings shows which version you run and checks for updates on the spot. The version on offer can be skipped with one press, and checking again brings it back.
- Foxy says so when you're offline: a banner sits above every view until the connection returns, and update checks wait instead of failing in silence.

### Fixes

- A call resumed from the popup records the Mac's audio again, not only the microphone.
- Recording survives Bluetooth headsets that promise one sample rate and deliver another.
- The microphone follows your input device when it changes in the middle of a recording.
- The computer-audio switch on a call's page shows what the recording actually uses.

### Improvements

- Foxy Live is signed by Seedext, so the installer and the app name their real publisher.

## 0.1.0 (2026-08-07)

First release.

### Features

- Foxy transcribes calls and voice memos live, from the microphone or from computer audio.
- A recording can be translated into a second language while it runs.
- Each recording gets a written summary that keeps up as the conversation goes on.
- Attach a PDF or Word file to a note, and Foxy picks up the names and terms inside it so the transcript spells them right.
- The app is available in English, French and Spanish, tray menu and popups included.
- The transcript lives in a panel that rises from the status pill.
- A call in progress is detected and offered for recording, with a native popup on macOS.
- A note exports as one Markdown file from its own menu.
- Transcription runs through the Foxy relay, so no AI provider key is stored on your Mac.

### Improvements

- The app is notarized by Apple, so installing it shows no security warning.
- First launch walks through the Microphone and System Audio Recording permissions once, and the choices stick.
- Setup asks for the relay secret on the same screen, and a new install already points at the hosted relay, so there is no address to look up.
- The database, recordings and attached files live in ~/Foxy, a folder you can find and back up. Older installs move themselves there on the next launch.
- Any text in the app can be selected and copied, and dragging the window no longer loses the selection.
- Settings is a set of cards, and every change saves itself.
- Sharing diagnostics is a setting, and it starts off.
