# DEAD AIR — PyroMania

**An original, browser-playable psychological horror strategy duel.** Inspired by the tension of hidden-information chamber games, but with original branding, interface, visuals, items, and synthesized sound effects.

## Play locally
Open `index.html` in a modern browser. Internet is needed to load the PeerJS library and Google Fonts; the game itself is a single HTML file.

## Online multiplayer
1. Open the site in a modern browser with an internet connection.
2. One player chooses **Private Table → Host a Table → Create room**.
3. Share the room code shown in the host tab.
4. Friends choose **Join a Table**, enter the code and a callsign.
5. The host starts when at least two players are connected. Supports up to four players.
6. Keep the host tab open throughout the match.

Online play uses PeerJS's public signalling service. It is a free convenience service, not a dedicated production server; availability and some network/firewall configurations may vary. For a commercial launch, replace this with a maintained authoritative server.

## Rules
- Each round loads a random mix of live and blank shells. Players know the counts, not the order.
- On your turn, use a limited tool or shoot yourself / a rival.
- A live shell deals damage. A blank fired at yourself keeps your turn; other shots pass the turn.
- Win two rounds, or have the highest round wins after three rounds.
- Tools: Glass Eye (peek), Bleed Valve (eject), Barrel Brace (double next live damage), Field Dressing (heal), Deadbolt (skip a rival's turn), Drain Cup (eject and keep turn).

## Controls
Touch-friendly buttons; mouse/touch input is not required for aiming. Works on desktop and mobile browsers.

## GitHub Pages
This repository includes `.github/workflows/pages.yml`.
1. Create a **public** GitHub repository named `PyroMania-Game` (or another name).
2. Upload the contents of this folder to the repository root, including `.github`.
3. Go to **Settings → Pages** and select **GitHub Actions** under Build and deployment.
4. Push to `main`. The included workflow publishes the game.

## Assets and licensing
The visual design is drawn using HTML/CSS/SVG and all sound effects are synthesized with Web Audio; no Buckshot Roulette game files, art, soundtrack, or extracted assets are included. Fonts are loaded from Google Fonts and PeerJS is loaded from unpkg at runtime. External asset libraries worth considering for future original 3D work:
- Poly Haven (CC0 models, textures and HDRIs): https://polyhaven.com/license
- Kenney Impact Sounds (CC0): https://kenney.nl/assets/impact-sounds

## Known prototype limits
- Online rooms use a public PeerJS signalling service and host-authoritative messages; this is a polished prototype, not hardened anti-cheat infrastructure.
- The multiplayer host must remain connected and should not refresh during a match.
- The game is 2D UI/illustration-based, not a 3D first-person game.
