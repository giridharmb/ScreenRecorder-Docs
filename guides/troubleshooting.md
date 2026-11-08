# Troubleshooting and FAQ

[← All guides](../README.md#user-guide) · [Get help](../SUPPORT.md)

## I cannot find a download

The app has not been publicly released yet. This repository is the documentation preview. See [release status](../RELEASES.md); there is no public installer to download at this time.

## No displays, apps, or windows appear

Check **System Settings → Privacy & Security → Screen & System Audio Recording** and enable Screen Recorder. Return to the app and refresh. If permission was just enabled, quit and reopen the app when macOS asks. Do not quit an active recording without saving it.

## A window is missing or its preview is blank

Open or restore the window, clear the search and application filter, then choose **Refresh windows & previews**. The default list shows on-screen windows. Enable **Include off-screen / minimized windows** to see the others. Minimized or hidden windows may show a restore-window placeholder or a labeled last cached preview instead of a current image. The chooser lists windows, not every browser tab. Move a tab to its own window if you need a separate source.

The gallery retries an empty or all-black image once, then shows **No preview image** or keeps a labeled last good preview. After restoring or changing the source window, refresh to try again. Previews are still images and are cached while you scroll.

A protected video or other restricted content can remain unavailable even when the rest of its window is visible. The app does not remove those restrictions. An unavailable preview is not proof that capture will succeed; make a short test.

## I see several windows with the same app name or title

Use the large previews and window numbers to select the right one. Separate running app instances are labeled separately. Activate the intended browser tab in the correct window and refresh the previews. Selecting or filtering by an app does not mean all of its tabs are individually selectable.

## Will Firefox keep recording if I use Chrome?

Yes, when you choose the specific Firefox window in **Window** mode. Switching apps does not retarget that window capture. Keep Firefox open and playback running. Switching tabs inside that same Firefox window changes what is recorded.

Display and Area modes record whatever is visible on the selected screen or rectangle, so Chrome can enter that picture. See [capture modes](capture-sources.md).

## Audio is missing, quiet, or doubled

Check **System / app audio** for computer playback and **Microphone / audio input** for your voice. Both off means a silent recording. Check microphone permission and the selected input device. Reconnect a disconnected input or choose System default before starting.

Leave the source player’s own volume up and unmuted. Lower the Mac’s speaker or headphone volume for quiet listening; that preserves original-level system audio. Turn up your playback volume to a comfortable level when reviewing a file recorded while the Mac was muted.

Other tabs in the selected app can contribute sound. Pause or mute unwanted playback there. If sound is doubled, use headphones or turn off microphone capture so it does not pick up the speakers as well. Test third-party mixers and external audio devices with a short recording. See [audio setup](audio.md).

## Record is unavailable or the source closed

Choose a valid display, app, window, or area, and allow any current save or conversion to finish. If a selected window closes, refresh and choose another; the app does not silently select a different window. For Application mode, also choose the intended display. For Area mode, drag a rectangle before recording.

## The main window disappeared

It may be hidden automatically when recording starts, or you may have closed it. Use the recorder icon in the menu bar to pause, continue, stop, or **Show Screen Recorder**. You can change the hide-on-start preference after saving.

## The stop shortcut does not work

Another app may already use **⇧⌘2**. Check the availability message in Screen Recorder and use **Stop & Save** in the menu bar. The start and pause shortcuts work only while Screen Recorder is active.

## Saving is taking a long time or failed

Wait for joining and saving to finish, especially after a long recording with paused sections. Keep enough free space for both the recorded sections and the final video. MP4 and MOV need no extra conversion software.

If the app reports a save failure, keep the recoverable files it lists. Confirm the destination drive is connected, writable, and has enough space. Avoid renaming or deleting in-progress recordings. Use [support](../SUPPORT.md) if you cannot recover the result.

## My chosen save folder needs access again

Use **Choose Save Folder…** in the error panel or **Settings → Storage & Formats → Choose Folder…**, then select the same folder in the macOS chooser. The app remembers this grant securely. Reconnect external drives first. An unavailable destination does not cause recordings to be silently saved elsewhere.

## The app crashes or macOS reports an installation problem

Check the supported macOS version and the build’s release notes. Reopen after a crash and look in your chosen recording folder for files that may have been kept. A forced termination can leave an incomplete file; recovery is not guaranteed.

If macOS displays a security warning, verify the download source and contact support rather than disabling security protections. Do not share a complete crash report publicly without checking it for personal information.

## Does the app record when the laptop lid is closed?

Do not rely on that. The idle-sleep preference does not prevent lid-close sleep, forced sleep, or shutdown. Keep the Mac awake and the source available throughout a recording.
