# Privacy, markers, and exports

[← All guides](../README.md#user-guide)

These optional tools are included in the 2.1 development preview. No public app download is available yet. Normal recording remains available on macOS 15+; on-device transcription has additional requirements below.

## Cover private areas and exclude applications

Open **Privacy controls…** in recording options, or **Recording tools… → Privacy & audio protection**. Add a solid mask and enter Left, Top, Width, and Height as percentages of the final video canvas. Positions start at the top-left; the whole rectangle must stay inside the canvas. You can enable, disable, or remove each mask, up to twelve. Invalid enabled masks block recording.

Choose **Preview protected source** to check placement. The preview does not create a recording and does not show presentation overlays; check a short recording if you use framing, a webcam, or annotations. Masks are applied after those overlays and permanently cover their final pixels in both working and completed video. They do not mute sound or change the original application. Window-gallery previews remain unmasked source previews.

For **Display / Area** capture, select applications to exclude. The exclusions also apply to additional display captures and their application audio. Previously excluded apps stay listed by identifier if they close. Selecting an excluded app/window directly is blocked. Clear exclusions to use the macOS picker. Exclusions do not hide another app's content copied into the selected source, isolate individual browser tabs, or remove room audio captured by a microphone.

Review masks whenever the source or presentation layout changes. Changing sources within a recording is blocked while masks are enabled; stop, choose the new source, and review first. Saved profiles also retain privacy choices.

## Optional audio protection

In **Recording tools… → Privacy & audio protection**, choose:

- **Prevent clipping (limiter & mix headroom):** limits individual captured peaks and reserves headroom when combining application sound and microphone tracks. This can reduce overall volume. It cannot repair clipping already present in the source.
- **Reduce quiet microphone noise:** applies an 80 Hz high-pass filter and a quiet-signal gate. This can soften quiet speech and is not general-purpose background-noise removal.
- **Lower app sound while speaking:** lowers application sound toward 25% while the enabled, unmuted microphone has an audible signal, then smoothly restores it. Background microphone noise can trigger it.

All three are off by default. They affect saved sound and optional separate audio files. Use a short sound check and headphones. Speaker volume remains independent of source-level recording; changing an app/player's own volume still changes its source sound.

## Mark moments and add notes

While recording or paused, choose **Mark Moment** in the menu bar or use **Shift-Command-M** by default. You can change the shortcut in Recording Tools. Floating Controls also lets you enter a short note before marking. Markers use the active recording timeline; paused time is excluded. They are navigation aids rather than frame-accurate edit points.

After saving, select a recording and open **More → Markers & Transcript…**. In **Markers & notes**, click a timestamp to play that moment, edit or remove a note, or add a marker in seconds. **Export Markers…** writes a new JSON sidecar in a folder you choose. Markers are kept locally and in recovery records. A separate display/audio companion receives the session's markers too.

## Make sharing copies

Select one or more recordings and choose **Organize → Make Sharing Copies…** or the context menu. Choose 540p, 720p, or 1080p and review the combined size estimate. Choose an output folder to queue new MP4 video or M4A audio copies. Originals stay intact and existing filenames receive a number rather than being replaced.

The presets use native macOS encoding. Size estimates are approximate and can be unavailable. A short, already compressed, or lower-resolution source may produce a larger file; inspect the result before sharing. These copies do not enable WebM or MKV output and need no FFmpeg installation.

Open **Exports & Transcription…** from the menu bar or Recordings tab to see progress and estimated time remaining. **Pause queue** holds waiting jobs; it does not pause the current encode. Cancel stops a selected job; Retry resubmits failed/cancelled jobs. Reveal Copy opens the completed file in Finder. Clear Finished or selecting finished rows and pressing Delete removes rows only, never media files.

Jobs run one at a time and wait while a recording or another file operation is active. Use **Run Queued** when ready. The queue belongs to the current app session; quit warns about waiting jobs. It is not restored after reopening.

## On-device transcripts and subtitles

In a recording's **Markers & Transcript… → Transcript** tab, choose a supported language and **Transcribe**. This requires macOS 26+, compatible hardware, and an Apple language model. If the model is missing, enable **Allow Apple to download the language model if needed** and retry. Model availability depends on the Mac, language, system, storage, and network connection. Other recording features do not require downloading a speech model.

The recording is processed on this Mac. There is no cloud-recognition fallback. Jobs appear in the same export queue and can be cancelled or retried. Silent files or unrecognized speech report an error. Re-transcribing replaces that recording's stored transcript after a successful result; cancelled/failed jobs keep existing text.

Search the transcript and click timestamps to play matching passages. Library search also finds transcript text and marker notes. **Export SRT… / Export VTT…** writes numbered, timestamped subtitles as a new file in your chosen folder. Recognition can be inaccurate; review text and timing before sharing. The app does not burn captions into video or provide a transcript text editor.

## Favorites, tags, and collections

Select recordings and use **Organize** to mark favorites, add tags, or assign a collection. Comma-separated tags are deduplicated. By default bulk edits append tags and leave a blank collection unchanged; **Replace existing tags and collection** replaces them and can clear them. Filters let you show favorites, a tag, or a collection. Library search includes tags, collection names, marker notes, and transcript text.

Organization does not move or rename media. Metadata stays in the app's local support storage and is associated with file paths. Rename through the app to preserve it. External moves/renames, uninstalling app data, and copying a recording to another Mac do not automatically carry this metadata. Export markers/subtitles separately when needed.

## Restart a take

During recording or pause, open **Floating Controls → Restart Take…**. The app first stops and saves the current take, then starts the same available source with a numbered Take filename and the configured countdown. Auto-stop and markers start afresh. If saving fails or the source changes/disappears, it stops and reports the problem rather than silently choosing another window.

The previous take stays saved by default. The optional checkbox moves its saved video and audio companions to macOS Trash after successful saving. Existing files are never overwritten. Review the choice carefully; a companion alignment JSON is kept in the output folder. Session Undo can restore trashed media while the app remains open, subject to normal folder/name checks.

## Align multiple display files

Additional display recordings share a capture clock, frame grid, and section end. Startup gaps are black/silent. The app saves an **alignment JSON** beside the videos and shows each file's section start, first-sample delay, and duration under **Markers & Transcript… → Display timing**.

This helps line up files in an editor. It does not guarantee physical frame synchronization or correct acquisition latency and dropped frames. Use a visible/audible reference when precise alignment matters. Paused intervals are removed from all files; inspect the actual results on your display setup.
