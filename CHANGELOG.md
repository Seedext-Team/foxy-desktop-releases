# Changelog

What changed in Foxy, newest first.

## 0.9.6 (2026-10-27)

### Features

- Notes open in tabs, and a tab can show two pages side by side. The drawer and Home have a new layout, and each project has its own colour.
- The summary has a page of its own. You edit it the way you edit your notes, and your changes sync to your other computers.
- The note's "⋯" menu can copy and duplicate the note. ⌘Z brings back a note you just moved to the trash.
- You can fix a finished line of the transcript where it is. Once you do, the summary offers to regenerate.
- The transcript panel can translate the whole transcript and still keeps the words as they were spoken. One button copies the transcript as the panel shows it.
- You can make the transcript panel wider or narrower. When the note needs the room, the drawer folds away, and in a narrow window the panel lies over the note.
- A highlighted word in the transcript shows the passages from your attached documents. Rest on the word for 3 seconds, or click it, and the box stays open: you can scroll the text around the word, and close it with its X.
- Help on a note page now walks you through that page.
- When Foxy runs from outside the Applications folder, it offers to move itself there so it can install updates.
- When your organization's monthly allowance for summaries and translation runs out, Foxy says so plainly, and live translation stops for the rest of that meeting.
- Claude Desktop keeps working when Foxy restarts or updates. To get this, connect Claude again once in Settings > Connectors.

### Fixes

- The transcript panel closes right away. Before, it paused for a moment first.
- The buttons at the top of the window stay in line with the window controls while you resize the window.
- A new user's Home no longer says "No meetings yet". An empty project's page says "No notes yet".
- "Jump to latest" appears only when the transcript is long enough to scroll.
- "Show more" under Recent appears only when there are more notes than the ones listed.

### Improvements

- The copy and hide buttons in the transcript panel no longer look like a window's buttons.
- The ring that shows where the keyboard is when you press Tab is now a thin line.
- A German or Spanish document no longer turns words like "Die" or "Los" into keywords. A long name such as "Microsoft Entra ID" now also highlights when someone says "Microsoft Entra".
- The DMG window shows Foxy, an arrow and the Applications folder, and nothing else.
- You pick a project's colour from twelve swatches.
- The Recent notes page has no lines between rows, and the Notes / Summary switcher sits on the left.

## 0.9.5 (2026-10-21)

### Features

- When live transcription has a problem, Foxy keeps trying for as long as you record and says nothing for the first minute. After that, the meeting banner shows one short line that names the cause, and the line goes away as soon as the transcript is live again. Foxy stops only when you or your administrator have to do something, and then it says what.
- A part of the transcript that is still missing now says what it waits for: a connection, the service, your administrator, or a sign-in. Before, it always asked you to go online.
- Messages about sign-in, summaries and translation now say what to do, in your language, and no longer show the server's own words.

### Fixes

- A summary now retries for up to 15 seconds when the service is busy, then says so.
- Translation treats a busy service as a short pause, and says it is paused only after a minute of failures.
- After a reconnect, the transcript's missing part closes as soon as the connection is back, even if nobody speaks. An outage now leaves one missing part instead of one per reconnect.
- Filling in a missing part of the transcript no longer loses turns when your sign-in needs to be refreshed at the same time.
- Foxy no longer signs you out when it can't read the server's answer to a session refresh; it tries again.

### Improvements

- When your administrator asks for new encryption keys, Foxy replaces its audio key at once and tells the administrator when all its keys are new.
- Foxy now tells Seedext's servers which version it is, so your administrator can see which computers need an update.
- Export diagnostics shows the error code of each failed request.
- The Project button in the agenda has the same rounded shape as Today.

## 0.9.4 (2026-10-16)

### Features

- Foxy now uses Seedext's production servers, which are set when the app is built, and the "Relay URL" setting is gone. After this update, each computer asks you to sign in again once: the sign-in screen says "Sign in again to keep using Foxy after this update." Your notes stay on your computer, and the same account opens them after you sign in. Foxy can't open your notes until you do, so sign in while you are online.
- The record pill is now a round record button at the bottom right of the note. While you record, a stop button slides out beside it, and only the stop button ends the recording; the record button then opens and closes the transcript.
- The transcript opens in a panel on the right of the window, from the record button or from a button next to the note's menu. The first recording of a note opens it, and each note remembers whether you left it open. A minus button in the panel's header hides it. The "Transcript" chip under the title is gone.
- The transcript panel has one language button, for the spoken language and the translation. It opens a menu with "Spoken" and "Translate to", and a change applies to new turns. The button is a grey pill that turns dark when you point at it. When the speech is already in the translation language, it reads "(paused)" and Foxy doesn't translate. A line above the turns says from what time the recording is translated.
- Each turn in the transcript shows the time it was said, and a day line separates turns said on different days. Search results show the time too, and the day when it differs from the note's day. A note you resume days later no longer shows times like "185:46:58".
- Every tooltip in Foxy now looks like the "New note" button's label, instead of the system's.
- A short tour points at Foxy's main controls after the first launch. Help in the drawer shows it again.
- Home lists your notes under "Recent notes", by when you last opened them on this computer, one line per note. A note shows a tag only while it records or when it failed.
- New notes no longer ask you to choose between Call and Note. Every note is just a note.
- "Join" on a calendar meeting's note opens the meeting link and records into that note. The recording ends when the call ends.
- Settings has a Sign out button next to the version, at the bottom of its sidebar.
- In Claude Desktop, the Connectors > Foxy menu lists the 20 notes at the top of Home, so you can attach one to a message.
- When your transcription hours for the month are used up, or Foxy is paused for your organization, Foxy says so in plain words when you record and on the minutes of a transcript that wait to be transcribed. When Foxy is paused for your organization, it also says so when you ask for a summary and during live translation; the monthly hours never stop summaries or translation. Foxy keeps the audio of the missed minutes for up to 30 days after the recording, and transcribes it when your hours go up, the month changes (in UTC) or the pause ends. Earlier versions showed a general error in these cases.

### Fixes

- "Auto" now detects the spoken language. Before, Auto kept transcribing in your interface language. The language button shows the language Foxy heard, and each turn is translated according to its own language.
- Live translation no longer stalls or freezes when the translation service is slow. The grey live text keeps moving, and finished turns don't wait behind a slow one.
- Claude Desktop keeps Foxy's tools after you quit or update Foxy. Before, Claude showed "Server disconnected" until you restarted it. If you quit Foxy, it stays closed; the tools work again once you open it.
- If you connect Claude while you are signed out of Foxy, the connection now waits for you to sign in. Before, Claude lost Foxy until you restarted Claude.
- A sign-in that is turned away for a reason other than your email domain no longer says that your domain is not allowed.

### Improvements

- The "Release candidate" update channel is now called "Beta".
- The note's chip row no longer shows a Recording chip.

## 0.9.3 (2026-10-13)

### Features

- Foxy Desktop is now called Foxy, in the menu bar, the tray, the window title, the Windows Start menu and the installer. On a Mac, an update keeps the "Foxy Desktop" name on the app in your Applications folder until you reinstall from the DMG. On Windows, the new installer replaces the old "Foxy Desktop" install and its shortcuts instead of adding a second copy.
- The record pill has a "Translate" list next to "Language". You can pick a language before or during a recording, and the translation starts with the next sentence. Foxy remembers your choice, starts on Disabled, and does not translate into the language being spoken.
- Every recording captures your computer's audio along with your microphone, so the "Use computer audio" switch is gone. If a Mac refused that permission, Foxy records the microphone alone and tells you.
- The installed version of Foxy shows at the bottom of the sidebar on the Settings page, on Mac and Windows. It no longer shows under your profile on Windows.

### Improvements

- Labeled speakers is paused for now: its setting is gone and recordings are not split by speaker. With translation moved to the pill, Settings no longer has a Transcription section.
- On Windows, a Claude or ChatGPT connection made before this version can't start Foxy when Foxy is closed. It still works while Foxy runs, and connecting the app again in Settings > Connectors > AI apps fixes it.

## 0.9.2 (2026-10-13)

### Features

- With a Seedext account, Settings > General > Updates has an "Update channel" setting: Stable, or Release candidate to get new versions before everyone else.
- On Windows, the sidebar shows which version of Foxy is installed, under your profile.

### Fixes

- Foxy trusts the same certificates as your computer. A Windows PC that was missing a root certificate could not connect until Windows Update ran; it connects now. When a connection fails, Foxy says what to check (the date and time, the proxy or the network), and on Windows the sign-in screen can open Windows Update.
- Foxy follows the computer's proxy settings.
- Every button and control stays readable when you point at it, and keyboard focus shows the same ring everywhere.
- On Windows in the dark theme, the language list in the record pill is no longer white.

## 0.9.1 (2026-10-12)

### Features

- Settings > Connectors > AI apps now offers Claude and ChatGPT only. Cursor and Claude Code are gone, and Foxy removes any connection to them when it updates.
- The transcript panel matches the rest of Foxy, and its lines start where your notes start. A button in its corner makes it tall for reading a call back, and Foxy remembers the height. It opens a little shorter than before.
- A "Transcript" chip under the title opens and closes the transcript. It replaces the row that sat in the middle of the note, and the panel has its close button back.
- The summary sits at the top of the note, folded to one line. Click it to read the whole summary; Foxy remembers whether you left it open. The line between the title area and the notes is gone.
- ⌘F also searches a folded summary and a closed transcript, and opens them to show what it found. It starts searching at two characters.
- "Projects" in the sidebar reads as a section title. It still folds, with its arrow after the word when you point at it.
- The record pill's level bars grow from their middle, like the ones in the notch, and both react more to your voice.

### Fixes

- "Create a project" stays greyed out until you type a name.
- Filled buttons and "Generate summary" are readable again when you point at them.
- The pill's sound-wave button and "Use computer audio" no longer fade into their background when you point at them.
- Search highlights in the transcript follow each key you type instead of keeping the previous search's.

## 0.9.0 (2026-10-09)


### Features

- Notes have a new editor. Headings, lists, to-do lists, quotes, code, tables and links format themselves as you type. "/" opens a menu of blocks, a bar over the selected text changes its style or adds a link, and ⌘K edits a link.
- Tables, to-do lists and highlights look the same in search results, in the trash and in Copy as HTML as they do in the note.
- A search page finds notes, transcripts, summaries, files, people, projects and meetings in the current workspace. A transcript or summary result opens the note at that passage.
- ⌘F finds words in the open note, its summary and its transcript. ⌥⌘F opens the search from any page.
- ⌘N starts a note, ⌘, opens Settings and ⌘\ shows or hides the drawer, from any page. The buttons show their keys when the pointer is over them.
- If the connection drops during a recording, Foxy keeps the audio and transcribes the missing part after the recording stops. The transcript marks where text is still to come, and the note's header says how many minutes are left.
- Foxy deletes a recording's audio when the recording stops, once its gaps are filled, or after 30 days at most. The "Keep audio files for" setting is gone.
- You can change the language during a recording. Foxy keeps what was being said, then goes on in the new language, and the record pill says "Switching to French…" while it does.
- Settings > Workspaces renames a workspace and, from a row's "…" menu, makes it the default. The default is the same on all your computers.
- Settings > Account has a Sync now button.
- The first sync of a computer merges the projects and workspaces that have the same name on both sides.
- Deleting a project asks whether to keep its notes or move them to the trash.
- Every delete asks in the same dialog, and if Foxy cannot delete, the dialog says why.
- An AI app can open a calendar meeting's note, and the note is linked to that meeting.
- The drawer button shows whether the drawer is open, and a round "New note" button sits beside it on every page.

### Fixes

- A pause in speech ends its line in the transcript. The next sentence was sometimes joined to the line before.
- The microphone's banner stays up until the microphone works again. A reconnection used to take it down while the microphone was still silent.
- Switching to AirPods during a recording no longer leaves the microphone dead until the end.
- A note hidden by a move on another computer comes back.
- No part of the window bounces past its edge on a trackpad drag.
- Every sentence Foxy shows starts with a capital and ends with a full stop.
- The record pill stays on one row. The window is now at least 960 pixels wide.
- The page's scroll bar stays clear of the window's edges and of the fades at the top and bottom.

### Improvements

- When a session expires, the record pill says so in one short sentence.

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
