# Baby Breakout online lobby prototype

Upload the **contents** of this folder to a GitHub Pages repository (index.html and assets/ at the same level). The host clicks Create lobby, copies the invite URL, and leaves the tab open. Guest opens the link, enters optional password, and clicks Join lobby. Host clicks PLAY after the guest joins.

Controls online: each player uses WASD, Shift to sprint, F to throw. Host is Baby 1; guest is Baby 2. Host is authoritative for the game state. Solo CPU is still available when not in an online lobby. If guest disconnects mid-match, CPU takes over.

Networking uses the PeerJS public signaling server and WebRTC, which require internet access and can fail behind some restrictive networks. GitHub Pages hosts static files only; it does not itself run a game server. Password is a lightweight lobby gate, not secure authentication, and is sent over the established WebRTC data channel. Do not reuse a sensitive password. Rooms only exist while the host is connected. This is a prototype, not production-grade anti-cheat or robust matchmaking.

## Audio
Music and sound effects are synthesized live in the browser (Web Audio), so there are no audio files and nothing to license.
- Menu theme (music-box lullaby), calm sneaking theme during play, and a faster chase theme when the babysitter spots a baby.
- Effects: button click, game start, pick up, bank, throw, babysitter hears something, babysitter spots you, caught, win, lose, tie.
- Press **M** to toggle music and **N** to toggle sound effects (or use the 🎵 and 🔊 buttons). The setting is remembered.
- Browsers only allow sound after a click or key press, so audio starts on your first interaction.
