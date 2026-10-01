# RevCord

A custom Discord-style frontend built for the browser with **no backend**.

## What works now

- Quick username-only local signup
- Real local persistence with localStorage
- Servers: create, switch, rename, delete
- Text channels: create, switch, send messages
- Voice channels: join live browser voice rooms
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

## Voice chat in the no-backend build

Voice channels use WebRTC for audio and BroadcastChannel for local signaling.

To test two local identities on the same machine, open RevCord in two tabs and use different test URLs such as `?user=Alice` and `?user=Bob`. Join the same voice channel in both tabs. Allow microphone access in both tabs.

The browser-only VC is not a multi-device account system. Different devices need a backend signaling layer (or a hosted signaling service) plus persistent user/channel data.

## No-backend limitation

A browser-only app cannot provide a trustworthy multi-device account system, persistent cross-device friends, or server-side message synchronization by itself. RevCord therefore keeps local state in the browser.

## Run

This is a static site. Open index.html from a local/static web server or deploy the repository to GitHub Pages.

## Next backend phase

A backend can later replace the local-only pieces with authentication, database-backed servers/channels/messages/friends, WebSocket signaling, and production WebRTC infrastructure.
