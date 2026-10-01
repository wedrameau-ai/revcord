# RevCord

A custom Discord-style frontend built for the browser with **no backend**.

## What works now

- Quick username-only local signup
- Real local persistence with localStorage
- Servers: create, switch, rename, delete
- Text channels: create, switch, send messages
- Voice channels: clicking one starts a voice call
- Video calls with WebRTC
- Microphone mute, camera toggle, and deafen
- Same-browser friend requests and friends
- Friend list call buttons
- Search/filter messages
- Dark and Midnight themes
- Compact layout and animation settings
- Keyboard shortcuts
- Privacy/local-data settings and reset
- Responsive desktop/mobile layout
- No seeded fake users or fake online member counts

## No-backend limitation

A browser-only app cannot provide a trustworthy multi-device account system, persistent cross-device friends, or server-side message synchronization by itself. RevCord therefore keeps local state in the browser.

For testing calls without a backend, open RevCord in two tabs/windows on the same browser and use two different local usernames. The tabs communicate through BroadcastChannel and establish the actual media connection through WebRTC. Camera/microphone permission is required.

## Run

This is a static site. Open index.html from a local/static web server or deploy the repository to GitHub Pages or another static host.

## Next backend phase

A backend can later replace the local-only pieces with authentication, database-backed servers/channels/messages/friends, WebSocket signaling, and production WebRTC infrastructure.
