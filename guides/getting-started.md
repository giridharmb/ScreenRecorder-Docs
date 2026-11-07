# Get started

[← All guides](../README.md#user-guide)

## Availability

Screen Recorder is preparing for a public release. **There is no public app download yet.** This guide explains the planned installation flow and how to use a preview build if one has been provided to you. Check [release status](../RELEASES.md) for announcements.

The app is designed for macOS 15 or later on Apple silicon and Intel Macs. You need enough free disk space for your recording. MP4 and MOV do not need extra audio drivers or conversion software. WebM is optional and requires a separate FFmpeg installation.

## Install a provided build

1. Open the Screen Recorder disk image (`.dmg`) supplied through the announced distribution channel.
2. Drag **Screen Recorder.app** to **Applications**.
3. If replacing an existing copy, finish and save any recording, then quit the old app first.
4. Open Screen Recorder from Applications.

Public download details will be added when the release is available. If macOS reports an unverified developer, damaged app, or another security problem, stop and check the download source and release notes. Do not disable macOS security protections to install it. See [support](../SUPPORT.md).

## Allow screen and audio access

1. In the app, click **Allow Screen Recording…**.
2. In System Settings, open **Privacy & Security → Screen & System Audio Recording** and enable Screen Recorder. The exact label can vary with macOS.
3. Return to the app and refresh the source list. If macOS asks you to quit and reopen the app, do so after saving any work.

Microphone permission is separate. The app asks for it when you start a recording with **Microphone / audio input** enabled. Leave that switch off if you do not need it. Permissions can be changed later in System Settings.

## Make your first recording

1. Choose **Display**, **Window**, **Application**, or **Area**. For a window, the app opens the **Choose Window** tab; select a preview and click **Use selected window**. For an area, choose a display and drag a rectangle.
2. Confirm the source title and snapshot. A snapshot is a still preview, not a live monitor.
3. Choose your audio. Turn **System / app audio** on for computer playback, **Microphone / audio input** on for your voice, or both off for a silent video.
4. Choose a quality preset. **Balanced**, **MP4**, and **H.264** are a straightforward starting point.
5. Enter a filename and choose a folder. The file extension follows the selected format.
6. Set a countdown if you need time to switch to another app, then click **Record**.
7. Use the recorder’s menu bar icon to **Pause Recording**, **Continue Recording**, or **Stop & Save**. You can also stop with **⇧⌘2** from another app when that shortcut is available.
8. Wait for saving or conversion to finish. Open the saved video and check the picture and sound before making a long recording.

The default destination is **Movies → Screen Recorder** in your home folder. Existing recordings are kept; duplicate filenames receive a number.

## Before a longer session

Make a short test with the same window, audio sources, and output settings. Keep the source window open and its video playing, connect your Mac to power, and make sure the destination drive stays connected. For Display or Area capture, consider using Focus to keep notifications out of the recording. Closing the laptop lid can interrupt capture.

Next: [Choose what to record](capture-sources.md) · [Audio setup](audio.md) · [Recording options](settings-and-files.md)
