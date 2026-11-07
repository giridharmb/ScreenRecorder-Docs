# Privacy

[← Screen Recorder](README.md)

This page describes the current Screen Recorder preview. It will be reviewed before the first public release and updated if the app’s behavior changes.

## Your recordings stay where you save them

The current app records and processes video and audio locally on your Mac. It has no recording upload service, account sign-in, advertising, or built-in analytics. Recordings are saved in the folder you choose. MP4 and MOV saving uses built-in macOS features. The app does not run an external converter.

If you select a folder managed by iCloud Drive, Dropbox, a network share, or another service, that service may sync or transfer the saved files according to its own settings. The app does not control those services. Opening an external download or support link uses your browser.

## Permissions and capture choices

- **Screen & System Audio Recording:** needed to list and preview capture sources and record the screen or application playback.
- **Microphone:** needed only when microphone or audio-input capture is enabled. The app requests this when starting a recording with that option on.

You can enable or revoke these permissions in System Settings. The app lets you choose a display, window, application, or area and whether to include system audio or a microphone. Pausing stops capture until you continue. Keep an eye on the recording state in the app or menu bar.

Display and Area recordings can include other apps, notifications, and anything visible in the selected location. Window or Application audio can include other playback in the selected application, including other browser tabs. Check the source and audio switches before starting.

## Previews, preferences, and temporary files

The app reads available application names and window titles to populate the chooser. Window-gallery snapshots use a bounded memory cache while the app runs, so scrolling and revisiting the chooser can reuse them. They are not saved as screenshot files or uploaded by the app. Off-screen windows are not automatically brought forward to obtain a preview. Main-window source snapshots are also previews, not uploaded images.

The Recordings tab reads filenames, relative folders, sizes, and filesystem creation/modification dates in your chosen save folder and its subfolders. This information stays on your Mac. The scan skips symbolic links, hidden files, and application packages; it does not automatically open or upload the videos. Optional naming rules can include the selected application’s name in saved filenames or folders.

Preferences such as the save folder and recording options are stored on your Mac. Recordings may use temporary sections in the destination folder while capture or joining is in progress. These are removed after a successful final save; recoverable files can remain after an error. Check the app’s message before removing them.

Removing the app does not remove recordings you saved in a separate folder. Manage those files in Finder. macOS can separately create diagnostic or crash reports according to your system settings; they are not the app’s built-in analytics.

## Public documentation and support

The screenshots in this repository are generated illustrations with fictional sample windows and content. They do not show a personal desktop or real recordings.

GitHub hosts this documentation and its public support issues. Visiting GitHub or posting an issue is separate from recording in the app. Anything you post to a public issue may be visible to others. Share only the details needed to explain the problem; do not include private recordings, credentials, personal window titles, or unredacted logs. See [support](SUPPORT.md).
