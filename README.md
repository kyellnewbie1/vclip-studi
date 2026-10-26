# VClip Studio — TypeScript video-editor starter

A runnable browser-based editing prototype built with React + TypeScript + Vite.

## Run locally
1. Install Node.js 20+.
2. Extract this folder and open a terminal inside it.
3. Run `npm install`
4. Run `npm run dev` and open the local URL Vite prints.
5. Run `npm run build` for a production build.

## Implemented in this starter
- Import local video, image, and audio files
- Timeline with draggable clips, multiple visual/audio lanes, trim handles, delete
- Preview with play/pause, seek, volume, aspect ratio and current time
- Basic image transform controls (position, scale, rotation), filters, speed
- Clip transitions selection and project JSON save/load
- Undo/redo history
- Export preview composition to WebM with selectable 720p/1080p, 24/30/60 FPS and bitrate (browser support varies)

## Important technical limits
This is a functional starter, not a full CapCut replacement. Browser WebM export uses MediaRecorder and the current preview compositor; complex multi-clip timelines, exact audio/video synchronization, codecs such as H.264/MP4, advanced keyframes, proxy media, and GPU effects need a dedicated render pipeline (e.g. FFmpeg/WebCodecs or a server render worker). Project JSON is saved in IndexedDB on the current browser/device. Imported media remains local unless the user exports/shares it.
