# Recording tools

[← All guides](../README.md#user-guide)

Open **Recording tools…** in recording options or the menu bar. These optional features extend the basic recorder; existing filename, folder, MP4, and original-level audio defaults stay the same.

## Check your sound

**Record a 5-second sound check** uses your selected source and audio inputs, skips the countdown, stops automatically, and opens the saved sample for playback. Choose a source and a safe destination first: this is a real local recording, not a simulated test. The first-run check guides you through permissions, destination, source, and playback.

Live meters show application/system and microphone levels separately, after recording gain and mute. Red **CLIP** means the signal reaches or exceeds full scale; reduce its level. A quiet meter can be normal for a silent source. Check playback before an important session.

**100%** preserves source level independently of your speaker/headphone volume. Gain above 100% can distort. The app/player's own volume still affects the source; use headphones to avoid microphone echo.

During a session, use **Mute app audio** or **Mute microphone** and their level sliders in **Floating Controls**. A disabled input cannot be enabled halfway through a session; enable it before starting. Controls also appear in the menu bar. Muting affects the saved sound, not just monitoring.

## Separate audio and audio-only capture

Enable **Record audio only (M4A)** to save sound without a video track. Screen/system-audio permission and a selected capture source are still required. Enable at least one audio input. Video format preferences remain available for your next video recording.

**Also save separate application and microphone files** creates M4A files in a companion `RecordingName-Audio` folder. The normal video contains combined sound; the companion files allow independent editing. They include your gain and mute choices and join paused sections without the pause interval. Inputs that produced no playable sound data have no companion file. No FFmpeg installation is needed.

## Saved profiles

Enter a profile name and choose **Save Current**. Profiles remember quality, audio/input choices, countdown, naming, save folder, and presentation options. They do not pin a particular window or browser tab. Choose the source separately before starting.

**Apply** restores a profile's options. Custom save folders still need valid macOS access; choose the folder again if a grant expires. **Remove** removes the profile, not its recordings.

## Floating controls and presentation

Enable **Show floating controls when recording starts**, or open **Floating Controls** from the menu bar during a session. The panel shows elapsed time, source, audio meters, free space, pause/continue, stop, mute/levels, annotations, and source switching. If video encoding falls behind, it shows dropped frames; reduce quality or presentation effects for the next session.

- **Webcam overlay:** opt in before recording, choose a camera, corner, and size. Camera permission is requested only when recording starts with the overlay enabled. The overlay is embedded in the saved video. Camera access can remain active while paused until the session ends.
- **Cursor spotlight:** adds a highlight around the pointer when it is inside the selected display/window/area. It does not reveal a pointer outside the selected source. For macOS picker sources, geometry is available on macOS 15.2 and later; if it cannot be identified, the spotlight is omitted. Inspect a test recording after switching sources.
- **Display keyboard shortcuts:** shows Command/Control shortcut combinations briefly in the recording. Ordinary typing is not displayed. It requires Input Monitoring permission, does not change that permission automatically, and is optional. Key combinations can reveal actions or sensitive context; leave it off when inappropriate.
- **Background & shadow:** None keeps the normal canvas. Indigo or Light adds a margin and shadow around the source.
- **Annotate…:** opens a drawing pad mapped to the video canvas. Draw freehand marks, undo a stroke, or clear them. Marks remain in the recording until cleared. This is a video annotation pad, not an annotation tool for the application being recorded.

Keep **Exclude Screen Recorder from display / area captures** enabled to exclude its control windows from those captures. Turning it off can include the recorder's interface in the video. Presentation features use additional processing power and are not applied to audio-only output.

## Global shortcuts

Start, pause/continue, and stop work across applications when their shortcuts are available. Defaults are **Shift-Command-R**, **Shift-Command-P**, and **Shift-Command-2**. In Recording Tools, use **Change…** and press a combination containing Command or Control. A conflict is reported beside the shortcut; choose another or use menu controls. **Restore Default Shortcuts** restores the defaults.

## Scheduled recording

Select **Start at** and choose **Schedule Recording**. Review source, destination, audio, and permissions before arming it. Keep the app open, the selected source available, and the Mac awake. Scheduling does not wake the Mac or bypass permission prompts. Quitting cancels the schedule after confirmation. A missed time after sleep is reported instead of silently starting late. Use **Cancel schedule** to change options.

The schedule belongs to the current app session; it is not a background service or recurring calendar task. Auto-stop still limits active recording time.

## Several displays and switching sources

In **Display** video mode, enable additional displays in Recording Tools. Each selected display receives a separate video file, controlled by the same pause/continue/stop session. Files use a shared capture clock and frame grid, with black/silent startup gaps and a common section end. A companion alignment JSON and the Display timing tab show startup delays and section times. Acquisition latency and dropped frames are not corrected; inspect alignment for precise editing. Additional files use a display identifier in the name. Each may contain that display capture's system audio. More displays need more storage and processing power. Additional displays cannot be combined with audio-only capture or the macOS picker.

**Choose with macOS…** offers Apple's source picker alongside the custom window gallery. During a single-source session, choose **Switch Recording Source…**, select a source, and **Confirm New Source**. **Keep Current Source** cancels the proposed change. Switching preserves the output dimensions; a different aspect ratio is fitted into the existing canvas. You can select while paused and continue when ready. Source switching is unavailable during a simultaneous-display session or while enabled privacy masks need review for a new source. Application exclusions require the custom Display/Area chooser.

A browser tab remains part of its browser window. Selecting a window does not independently pin one of its tabs.

## Storage, interruptions, and recovery

Recording requires at least 750 MB of free space at the start. During recording the app checks capacity, warns when space is low, and stops to reserve room for finalization. Space estimates cannot guarantee success if another application fills the drive. Keep external drives connected.

Sleep, display changes, device disconnection, and capture-stream interruptions can pause or end capture. Review the message, source, and devices before explicitly continuing, or stop to save completed sections. Starting/resuming failures retain recovery files when available. Sleep prevention does not override closing the laptop lid or shutting down.

After reopening, **Recover interrupted recordings…** lists saved recovery records. **Recover / Save As…** checks playable sections and saves a new recording, including separate files for finalized additional-display sections. **Keep for Later** leaves the record intact. Original recovery files are retained after recovery. A damaged or unfinished section may not be playable and is not guaranteed recoverable. Do not move, rename, or delete recovery files before recovery.

## Trim, rename, share, and filter

In **Recordings**, select one file and choose **More → Trim & Save a Copy…**, or right-click. Enter start/end seconds, preview the start, and save to a new filename. MP4/MOV video and M4A audio use native macOS tools. Trimming may re-encode and take time; originals remain unchanged and existing destinations are never replaced.

**Rename…** changes the selected completed file's name while preserving its extension. Existing names are never overwritten. **Share…** opens the system share choices for selected files; nothing is uploaded merely by opening the menu. Choose a service and recipient yourself.

Thumbnails load as rows appear. Select a recording to see duration, resolution, codec, and its known source application. **Date** filters Today, Last 7 days, or Last 30 days using filesystem dates. **Application** uses source information saved for new recordings; older/imported files show **Unknown / imported**. External moves or renames can lose that association. Metadata and previews remain local.

For privacy masks, optional audio protection, markers, restart take, sharing copies, transcripts, tags, collections, and export queue controls, see [Privacy, markers, and exports](privacy-markers-and-exports.md).
