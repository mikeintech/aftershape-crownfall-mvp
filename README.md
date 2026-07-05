# AFTERSHAPE Crownfall MVP

Static browser build for GitHub Pages.

## Run locally

Open `index.html` in a browser.

Or run the local static server:

```sh
npm start
```

Then open `http://localhost:4173`.

## Publish on GitHub Pages

1. Put this folder in a GitHub repository.
2. Enable GitHub Pages for the branch/folder that contains `index.html`.
3. Open the Pages URL in a browser.

## Online multiplayer MVP

This build uses PeerJS/WebRTC so GitHub Pages can stay static.

Host:
1. Enter your name.
2. Click `HOST ONLINE`.
3. Share the shown room code.
4. Wait for players to appear in the lobby seats.
5. Click `ENTER THE ARENA` to start.

Join:
1. Enter your name.
2. Enter the host's room code.
3. Click `JOIN ROOM`.
4. Wait for the host to start.

The host browser owns the match simulation. Joiners send input to the host and receive snapshots back. If the host tab closes, the room ends.

## Controls

Desktop:

- WASD: move
- Space: jump
- Shift: dash, or ghost nudge after knockout
- E: release crown
- Left mouse: shove
- Right mouse: shape ability

Mobile:

- Drag anywhere: move
- Tap anywhere: context action
- Context action does dash, shove, ability, or ghost nudge depending on the situation
- Crown pickup is automatic

## Arena MVP

- Four center ramps
- Four bounce pads
- Two pit gaps
- Two moving platforms
- Two cover blocks and two columns
- Panic Mode shrinking safe ring
- Outer panels fall away during Panic Mode

## Current limitations

- This is not the final Node/Socket.IO/Rapier authoritative server.
- Public PeerJS signaling may be blocked on some networks.
- Best for quick friend testing, not competitive/desync-proof play.
