# Changelog

What changed in Foxy, newest first.

## 0.5.0 (2026-08-19)

### Features

- You sign in with a Microsoft work account. Foxy's first screen has one button, the button opens your browser, and Foxy is signed in when the browser comes back. There is no secret to paste any more, and Settings shows which account Foxy runs under.
- Signing out keeps your notes. Everything local still works; recording, transcription and summaries stop, each with a sentence that says to sign in. An old pasted secret is removed by the same button.

### Fixes

- A refused or failed sign-in ends right away, with the reason in the browser tab and next to the button. It used to sit on "Waiting for your browser…" for five minutes.
- A session revoked by an administrator stops looking signed in within fifteen minutes, and Record closes instead of writing a recording nothing will transcribe.
- A brand-new install starts at the sign-in screen. It used to skip it and offer a Record button that failed when pressed.

### Improvements

- The pages your browser shows during sign-in look like Foxy: the app's paper background, one sentence, nothing to load and nothing to run.

## 0.4.0 (2026-08-17)

### Changes

- Foxy is now called Foxy Desktop. The new name shows in the title bar, in the menu bar and in the System Settings privacy lists. Nothing else moves: the microphone and computer-audio permissions you already gave still hold, your recordings are where you left them, and your relay secret is still saved.

### Fixes

- Clicking the Dock icon brings the window back after you close it. Until now only the menu bar could do that.

## 0.3.1 (2026-08-14)

### Features

- A waiting update shows through a closed drawer. A pulsing dot sits on the drawer button until you open it; the Update button is inside, where it always was.

### Fixes

- The buttons along the top of the window stay lined up with the traffic lights. macOS moves the lights between window states and resets them after fullscreen, so Foxy now asks the window where they are instead of trusting a fixed number.

## 0.3.0 (2026-08-13)

### Features

- Foxy stops recording on its own when the call it offered to record ends. A recording you started yourself keeps going, and so does one that belongs to a different call.
- A recording whose microphone dies now carries on with the computer's audio instead of ending. A warning on the note says your own voice is no longer being transcribed, and the recording closes itself once everything has been quiet for the delay you set.

### Fixes

- A recording whose microphone stops sending anything closes itself after the inactivity delay. It used to run until someone noticed, because the delay counted audio rather than time.
- A call where only the other side speaks stays open with speaker labels on, instead of stopping itself mid-sentence.
- A recording that loses the microphone and the computer's audio ends itself rather than claiming to record until you press Stop.
- A full disk warns you and keeps transcribing the call. It used to cost you the computer's audio.

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
