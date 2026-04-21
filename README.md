# Music Player

A polished React music player built with Vite, Tailwind CSS, GSAP, and the YouTube IFrame API. It presents a glassmorphic full-screen player, animated track artwork, and a searchable queue for managing playback.

## What The Project Does

This app plays a curated queue of tracks sourced from YouTube IDs in [src/data.js](src/data.js). The main player UI is assembled in [src/App.jsx](src/App.jsx), while [src/context/PlayerContext.jsx](src/context/PlayerContext.jsx) manages playback state, queue updates, preloading, repeat modes, shuffle behavior, and media-session integration.

The interface includes:

- A central now-playing card with animated artwork and track metadata
- A visualizer backdrop that reacts to playback state
- Transport controls for play, pause, next, previous, seek, shuffle, and repeat
- A queue drawer with search, drag-and-drop reordering, and per-track actions
- Track preloading and quick switching for a smoother listening experience

## Why The Project Is Useful

This project is a compact example of a modern media player built around real playback state instead of static UI mockups. It is useful if you want to study or reuse:

- A React context architecture for media playback
- YouTube-backed audio playback with hidden player instances
- Responsive UI patterns for a music app
- Accessible controls and keyboard-friendly queue interactions
- Lightweight animation and preloading strategies for smoother transitions

## How To Get Started

### Prerequisites

Use a current Node.js LTS release and npm.

### Install And Run

```bash
npm install
npm run dev
```

Vite will print the local development URL in the terminal, typically `http://localhost:5173`.

### Build For Production

```bash
npm run build
npm run preview
```

### Lint The Codebase

```bash
npm run lint
```

### Update The Track List

Tracks live in [src/data.js](src/data.js). Each entry follows this shape:

```js
{
	id: '1',
	title: 'Track title',
	artist: 'Artist name',
	youtubeId: 'VIDEO_ID',
	poster: 'https://i.ytimg.com/vi/VIDEO_ID/hqdefault.jpg',
	color: '#e62135'
}
```

Add, remove, or replace tracks there to change the queue shown in the app.

## Where To Get Help

If you need to understand how the app works, start with these files:

- [src/App.jsx](src/App.jsx) for the top-level layout and drawer wiring
- [src/context/PlayerContext.jsx](src/context/PlayerContext.jsx) for playback and queue logic
- [src/components/PlayerControls.jsx](src/components/PlayerControls.jsx) for transport controls and scrubber behavior
- [src/components/TrackDrawer.jsx](src/components/TrackDrawer.jsx) for queue search, actions, and drag-and-drop
- [src/components/TrackInfo.jsx](src/components/TrackInfo.jsx) for the now-playing artwork and metadata display
- [src/main.jsx](src/main.jsx) for app bootstrap and error handling

For project-specific help, open an issue or submit a pull request with the problem, reproduction steps, and any relevant screenshots or logs.

## Who Maintains And Contributes

This repository is maintained by darshan3187.

Contributions are welcome through pull requests. Keep changes focused, follow the existing React and Vite structure, and update the relevant source file references in this README if the player flow changes.
