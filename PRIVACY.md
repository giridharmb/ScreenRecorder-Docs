# Privacy

[← Screen Recorder](README.md)

This page describes the current Screen Recorder preview. It will be reviewed before the first public release and updated if the app’s behavior changes.

## Your recordings stay where you save them

The current app records and processes video and audio locally on your Mac. It has no recording upload service, account sign-in, advertising, or built-in analytics. Recordings are saved in the folder you choose. MP4 and MOV saving uses built-in macOS features. The app does not run an external converter.

If you select a folder managed by iCloud Drive, Dropbox, a network share, or another service, that service may sync or transfer the saved files according to its own settings. The app does not control those services. Opening an external download or support link uses your browser.

## Permissions and capture choices

- **Screen & System Audio Recording:** needed to list and preview capture sources and record the screen or application playback.
- **Microphone:** needed only when microphone or audio-input capture is enabled. The app requests this when starting a recording with that option on.

You can enable or revoke these permissions in System Settings. The app lets you choose a display, window, application, or area and whether to include system audio or a microphone. Pausing stops screen and audio capture until you continue; an enabled webcam can remain active as described below. Keep an eye on the recording state in the app or menu bar.

Display and Area recordings can include other apps, notifications, and anything visible in the selected location. Window or Application audio can include other playback in the selected application, including other browser tabs. Check the source and audio switches before starting.

## Previews, preferences, and temporary files

The app reads available application names and window titles to populate the chooser. Window-gallery snapshots use a bounded memory cache while the app runs, so scrolling and revisiting the chooser can reuse them. They are not saved as screenshot files or uploaded by the app. Off-screen windows are not automatically brought forward to obtain a preview. Main-window source snapshots are also previews, not uploaded images.

The Recordings tab reads filenames, relative folders, sizes, and filesystem creation/modification dates in your chosen save folder and its subfolders. This information stays on your Mac. The scan skips symbolic links, hidden files, and application packages; it does not automatically open or upload the videos. Quick Look opens only when requested. Confirmed cleanup moves selected completed videos to macOS Trash. Session Undo uses local, in-memory file-access information; it does not upload files or erase Trash. Optional naming rules can include the selected application’s name in saved filenames or folders.

The app uses macOS App Sandbox. Movies-folder access supports the default destination. Custom-folder access is granted through the standard macOS chooser and retained using a local security-scoped bookmark. If this permission becomes invalid, you can choose the folder again. The app does not request unrestricted filesystem or network access.

Preferences such as the save folder and recording options are stored on your Mac. Recordings may use temporary sections in the destination folder while capture or joining is in progress. These are removed after a successful final save; recoverable files can remain after an error. Check the app’s message before removing them.

Removing the app does not remove recordings you saved in a separate folder. Manage those files in Finder. macOS can separately create diagnostic or crash reports according to your system settings; they are not the app’s built-in analytics.

The Privacy Policy, User Guide, and Support links are available in the app’s Settings and Help menu.

## Public documentation and support

The images use fictional sample content only. Historical preview screenshots show a separate demo app and demo video files; the menu-bar image is an illustration. They do not show personal desktops, private browser tabs, or personal recordings.

GitHub hosts this documentation and its public support issues. Visiting GitHub or posting an issue is separate from recording in the app. Anything you post to a public issue may be visible to others. Share only the details needed to explain the problem; do not include private recordings, credentials, personal window titles, or unredacted logs. See [support](SUPPORT.md).

## Optional recording tools

Camera access is requested only when starting with the webcam overlay enabled. Camera frames are composed locally into the recording; the camera can remain active while the session is paused. Turn the overlay off before starting if you do not want camera access.

Optional shortcut display requires Input Monitoring. While enabled for a session, the app receives key events and displays only Command/Control shortcut combinations briefly in the saved video. Ordinary typing is not displayed and there is no separate keystroke log or upload. Disable shortcut display when key combinations could reveal sensitive actions or context. The app does not automatically grant or change system permissions.

Local recovery records store the intended filename, working-file locations, session date, and folder-access bookmarks. They remain in the app's support storage until successful saving/recovery. Unfinished media remains in the chosen recording folder; recovery preserves originals. Local profile and application-filter information also stays in app preferences. Optional companion audio files are separate recordings and need the same care as the main video.

Opening Share does not send a file. Choosing and completing a share through another app or service is controlled by that service and its privacy policy. Thumbnails, audio analysis, and trimming use native local media processing. A scheduled recording requires the app to stay open; it does not use a remote scheduler.
