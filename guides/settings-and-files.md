# Recording options and files

[← All guides](../README.md#user-guide)

## Quality and video

Choose a preset, then adjust resolution and frame rate if needed:

| Preset | Resolution limit | Maximum frame rate |
| --- | --- | --- |
| Compact | 720p | 24 fps |
| Balanced | 1080p | 30 fps |
| High | 1440p | 60 fps |
| Original | Native / Retina, subject to codec limits | 60 fps |

Resolution choices also include 4K. The source’s aspect ratio is preserved, and a small window is not enlarged just to reach the selected resolution. A portrait window stays portrait. A selected frame rate is a maximum; a static screen may produce fewer frames.

**H.264** is the compatibility choice. **HEVC** can produce smaller files but needs a compatible player. Capture is limited to a 4K envelope for H.264 or an 8K envelope for HEVC, depending on the source and Mac. Recording is SDR. There is no manual bitrate control in the current preview.

## Before and during recording

- **Countdown:** 0–30 seconds. Use zero to start without a countdown. The countdown can be cancelled.
- **Show cursor:** include the pointer in the picture.
- **Highlight mouse clicks:** make clicks easier to follow.
- **Include child windows:** include associated sheets and dialogs where supported.
- **Auto-stop:** stop after the chosen number of active recording seconds, up to 86,400. Zero means no time limit. Paused time does not count toward the limit.

Settings also let you hide the main window when recording starts, exclude Screen Recorder from Display or Area capture, prevent idle system sleep, play a countdown sound, and reveal the saved recording in Finder. Sleep prevention does not override closing the laptop lid, forced sleep, or shutdown.

Options are locked while recording or saving. Finish the current session before changing them.

## Pause, continue, and stop

Use the recorder’s menu bar icon to **Pause Recording**, **Continue Recording**, or **Stop & Save**. Main-window buttons provide the same recording controls. While paused, capture stops and the elapsed timer freezes. The saved video joins the recorded sections without the paused interval. Stopping while paused saves the completed sections.

Closing the main window leaves the app in the menu bar. Choose **Show Screen Recorder** to reopen it. Quitting during a session offers to stop and save first; allow saving to finish.

| Shortcut | Action | Where it works |
| --- | --- | --- |
| ⇧⌘R | Start recording | While Screen Recorder is active |
| ⇧⌘P | Pause or continue | While Screen Recorder is active |
| ⇧⌘2 | Stop and save, or cancel countdown | Across apps, if the shortcut is available |

If another app owns the global shortcut, Screen Recorder reports it as unavailable. Use the menu bar controls instead.

## File formats

| Format | Use it for | Extra software |
| --- | --- | --- |
| MP4 (default) | General playback and sharing; H.264 is a useful starting point | None |
| MOV | A QuickTime movie or a workflow that expects MOV | None |
MP4 and MOV are recorded using built-in macOS features. No FFmpeg installation or extra conversion software is required. WebM and MKV export are disabled. An older saved WebM/MKV preference automatically switches to MP4, keeping your other preferences.

Choose your preferred format in the recording options or **Settings → Storage & Formats**. The app remembers it for future recordings. Changing the filename extension does not choose a different format.

If joining or saving fails, recoverable recorded files are kept and the app displays their locations. Do not delete those files until you have checked and recovered the recording.

## Folders, filenames, and free space

Choose a destination and filename before starting. The default is **Movies → Screen Recorder** in your home folder. The extension follows the selected format; you do not need to type it. If a filename already exists, the app uses a numbered name instead of replacing it.

Keep enough free space for the whole session, including extra space for joining paused sections. A successful free-space check at the start cannot guarantee room for an unlimited recording. Keep external drives connected and avoid moving the destination folder while recording.

The existing filename and destination defaults stay the same. For optional prefixes, suffixes, naming templates, date subfolders, or app-based grouping, see [Naming, folders, and your recordings](organizing-recordings.md). Existing recordings are not renamed or moved by these rules.

## More menu bar actions

- During recording, see the destination filename, elapsed active time, and encoded size. Open the actual recording folder or copy the intended final path. The final file becomes available after saving finishes.
- Use **Recordings & Storage** to open the separate recordings tab, including while a session is running.
- After saving in the current app session, **Open Last Recording**, **Reveal Last Recording**, **Copy Last Recording**, or **Copy Last Recording Path** are available. Copy File puts the video on the clipboard for pasting into Finder or another compatible app; it does not upload it.
- While idle, **Next Recording** lets you change the preferred format, system/app audio, microphone, and countdown. Microphone permission is still requested only if needed when recording starts.
- **Open Save Folder** opens your base destination; **Open Recording Folder** opens the current nested destination during a session.

Completed files can also be opened, revealed, or copied from the [Recordings tab](organizing-recordings.md#recordings-tab-and-storage-statistics). Move or delete completed recordings with Finder after saving finishes.

## Updates and removal

The current preview does not automatically download or install app updates. When public builds become available, follow [release announcements](../RELEASES.md). Finish recording and quit the app before replacing it.

To remove the app, first stop and save, then quit it and move Screen Recorder from Applications to Trash. Recordings in your chosen folder remain separate files; remove them in Finder only if you no longer need them. You can revoke recording or microphone permission in System Settings.
