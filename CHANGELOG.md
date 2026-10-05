# Changelog

What changed in Foxy, newest first.

## 0.8.2 (2026-10-05)

### Features

- Your notes are encrypted on your computer, and each account has its own. Signing in opens your notes and signing out locks them; someone else signed in on the same computer sees only theirs. Recordings are encrypted as they record, and the keys renew themselves without you doing anything.
- The notes already on your computer move into the account you sign in with.
- A Security panel in Settings says in plain words whether your notes are protected.
- Your notes sync between your computers, encrypted, through a folder Foxy keeps in your own OneDrive or Google Drive. Edits made on two computers merge, down to the words in a note. If a note is being recorded on one computer, the other one says so, and Settings > Account lists your computers.
- On a new computer, signing in brings your notes back.
- AI apps on your computer can read your notes. Settings > Connectors connects Claude, ChatGPT and Codex, Cursor and Claude Code in one click, and Activity shows what each app asked for.
- If you allow it, an app can also create, rename, move and trash notes, workspaces and projects. Only you can empty the trash. After you connect ChatGPT, Foxy can restart it so it loads Foxy.
- Deleting a note moves it to the trash, with an Undo. In the trash you can read a note and put it back; "Empty trash" is the only way to delete one for good.
- Foxy has a dark theme. Settings offers System, Light and Dark, and the light theme now uses cool greys.
- A calendar meeting's note starts with the invitation's guests and agenda, says where the meeting is, and has a Join button.
- The agenda on Home covers the days around today.
- The recording indicator shows on every screen, including the ones without a notch.

### Fixes

- A call during a calendar meeting records into that meeting's note. It used to land in a note called "Microsoft Teams meeting".
- A booking tool's "[1 événement]" placeholder stays off the agenda.
- Claude Desktop shows Foxy's icon in its connectors list.
- Claude on Windows can install Foxy. On Windows, ChatGPT and Codex also get lines to paste when Foxy cannot edit their settings.

### Improvements

- The project menu lists the current project first, has more room, and creates a project from its footer.
- The participants list names your own row after you.
- The drawer's resize line is thinner and fades out at both ends.
- A note fades out under the record pill, and Home's titles and times are lighter.
- "New note" sits evenly in the window's corner.
- Settings opens on Account.

## 0.8.1 (2026-09-28)

### Fixes

- You can switch "Use computer audio" off on a call. Notes opened from a calendar meeting or started from the call offer used to lock it on, so a call could never be recorded from the microphone alone. It still starts on.
- Filled buttons, Record included, get lighter when the pointer is over them. They used to turn from near-black to black, and the change was invisible.

### Improvements

- "New note" on Home is a filled button, black with white text.

## 0.8.0 (2026-09-28)

### Features

- Notes live in projects. The drawer shows a Projects tree under Home, each project unfolds into its notes, and a note that belongs to no project waits under "No project".
- Projects and notes can be dragged in the drawer. A project moves to a new place in the list; a note moves within its project, into another one, or onto "No project".
- Every drawer row has a menu, behind its "…" button or a right-click. A note can be renamed, copied as Markdown, duplicated or deleted; a project can be renamed or deleted, and deleting it keeps its notes.
- The drawer is as wide as you drag it, from 234 to 360 pixels, and it remembers the width. A name too long for it fades into an ellipsis.
- You can have more than one workspace. The profile button at the foot of the drawer switches between them and creates new ones. Settings lists them with their note counts, and deleting one moves its notes, files, projects and vocabulary into the workspace you pick.
- Foxy reads your calendar. Home shows the day's next three meetings in an "Up next" card, a meeting offers to record itself when it starts, and its row opens the meeting's note. The access is read-only and stays on your computer.
- A calendar meeting can be filed in a project straight from Home, and its row names the project under the title.
- Signing in with Microsoft or Google connects your calendar in the same consent. Foxy now talks to the provider itself, and the provider's tokens never leave your computer.
- Chips under a note's title show its date and time, its participants, its project and its attached files with their sizes. Click one to change it.
- Settings has four panels, reached from the drawer: General, Account, Workspaces and Connectors.
- A workspace keeps its own vocabulary, typed in Settings. Transcription listens for those words first, and the summary spells them the way you typed them.
- The notch indicator wears the Foxy mark and sits evenly on both sides of the notch.

### Fixes

- Leaving a note keeps what you typed. Back, Forward, Home, switching workspace, quitting and restarting for an update all save first; the last keystrokes of a note, or all of a new one, used to go missing.
- The first letter typed into an empty notes box no longer knocks you out of it.
- A new note with text on it can be deleted from its menu.
- Home drops the red recording pill as soon as a take stops.
- Signing out stays signed out. A session refresh landing at the same moment could sign you back in.

### Improvements

- A note you start by hand keeps the title "Note" until you type another. Foxy no longer renames it after the first words spoken.
- A note you typed and never recorded is dated and sorted like any other. It used to sit under "Draft", on no day at all.
- The relay address is built in, and the setting only overrides it. Clearing the field goes back to the default.
- Sign-in is the only way in. The old pasted access key is gone, so an install that still used one has to sign in.

## 0.7.0 (2026-09-10)

### Features

- You can sign in with Google as well as Microsoft. The first screen shows one button per sign-in the relay has been given, so a team on Google Workspace no longer needs a Microsoft account to get in.
- A document you attach stays where you put it. Foxy reads its text once and keeps that; it used to also copy the file into a folder of its own inside ~/Foxy that nothing ever read back. An upgraded install deletes the old copies at launch.
- Auto starts on the language the app is in and keeps listening. The dropdown reads "Auto (French)" from the first second instead of guessing blind, three confident turns in another language move it, and one quoted sentence does not. Transcription gains Spanish, and the interface gains German.
- Transcripts come back punctuated, and every block starts with a capital letter. A French recording used to arrive as a handful of 30-second paragraphs with no full stop anywhere in them.
- Foxy updates itself on Windows. Until now only Macs were offered an update.
- App-health records are deleted after fourteen days. They used to pile up with nothing ever removing them.

### Fixes

- A relay that accepts the connection and then answers nothing no longer freezes the live transcript. Foxy gives up after two turns, says so once in a banner, and picks translation back up when the relay starts answering again.
- Foxy offers to record a call only when recording would work. Signed out, microphone denied or relay unreachable used to get the offer anyway, and Record ended in a red banner every time.
- The application log reads in your own time, with the offset written beside it. Every line was stamped UTC, so reading one meant converting it by hand.
- Signing in works on Windows. The address handed to the browser was cut in half at the "&", and the relay then refused its own sign-in link.
- The last thing said before you press Stop reaches the transcript. The drain allowed the relay two seconds, and a hosted one needs more than that.
- A CV keeps its vocabulary when Foxy derives keywords from it. PostgreSQL, gRPC, iOS, C++, CI/CD and a dozen more were dropped before the recording had started.

## 0.6.2 (2026-09-01)

### Fixes

- An update offer that has been sitting in the drawer follows the newest release. If Foxy was left running with one version on offer while a newer one came out, pressing Update installed the older one and the newer one showed up only after the restart.

## 0.6.1 (2026-09-01)

### Fixes

- The sound-wave bars each answer to the sound. They used to hand one reading down the row, so every word drew the same wave sliding across the meter.
- The dot that says an update is waiting sits on the corner of the drawer icon. It sat on the corner of the button around it, a little way off the icon.

## 0.6.0 (2026-08-31)

### Features

- Foxy shows a recording at the notch. On a Mac with a notch, a red dot, the name and a live sound level sit on the menu bar either side of the camera. Point at them and the strip opens downward with the elapsed time and a Stop button; click anywhere else on it and the window comes up.
- The sound-wave bars beside the Record button follow the microphone. They used to move at a fixed rate whatever the room was doing.

### Fixes

- The clock at the notch counts. It drew the same second for the whole recording.

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
