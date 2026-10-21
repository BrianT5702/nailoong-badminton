# Nailoong Badminton 🏸

A little browser badminton game starring Nailoong. No install needed: open the link and play on a laptop, phone or tablet.

## Characters (v15)

Press **Play!** and pick your character (and your opponent, or Random). Every character has six stats (Power, Speed, Jump, Control, Reach, Stamina) and one **special move**.

- **Nailoong** is the reference all-rounder: every stat is 6/10, no weakness.
- Nailoong-universe characters use the official art, drawn unedited: **Nailoong**, **Berry** and **Bombloong** (暴暴龙, from nailoong.com).
- The comic/cartoon guests (Spider-Man, Hulk, Iron Man, Captain America, Thor, Black Panther, Flash, Batman, Superman, Wonder Woman, Naruto, Goku, Pikachu, Doraemon) are **original fan-made chibi drawings** made in code by this game, recognisable by their colours and costume motifs. No studio art or logos are used.
- Every non-champion character has the same 36-point stat budget, so strengths come with weaknesses.
- **Stamina** (green bar under you): running, jumping, lunging and smashing cost it; it comes back when you stand still and quickly between points. Below 30% you are slower, jump lower, your timing window shrinks and smashes are weaker. At 0 you can't jump-smash.
- **Special meter** (gold bar): good shots and points fill it. When it is full press **Special** (default **I** for P1, **'** or **Num 6** for P2) to use your character's special.
- The roster is one table (`CHARS` in index.html): one entry per character with its art, stats and special, so characters are easy to add, rename or remove.

**Fan game notice:** this is a free, non-commercial fan game made as a gift. Nailoong, Bombloong and related characters belong to 第七印象 (Seventh Impression). All other characters belong to their respective owners (Marvel/Disney, DC/Warner Bros., Shueisha, The Pokémon Company, Fujiko Pro, etc.). No affiliation or endorsement is implied.

## How to play

**All keys can be changed:** press **⌨ Controls** on the title screen or in the pause menu (or "change keys" under the help). Click a key, press the new one (Esc cancels, Delete removes, up to 4 keys per action). If a key is already used, the two actions swap keys or the old one is freed. Anything left unbound shows in red. Your keys are saved in your browser (`localStorage`, key `nailoong.keybinds.v1`), so they're still there next time. The in-game help always shows your current keys. The table below lists the **default** keys.

| | Move | Jump | Clear (punch / high, by timing) | Smash | Drop / Net shot |
|---|---|---|---|---|---|
| Player 1 | A / D | Space | J | K | L |
| Player 2 | ← / → | ↑ (or Numpad 0) | , or Enter (Numpad 1) | . (Numpad 2) | / (Numpad 3) |

- Lunge for far shots: Player 1 Left Shift or Q, Player 2 Right Shift or ; (Numpad 5); or double-tap a direction
- In 1-player and online mode your player also answers to the Player 2 keys (arrows, , . / and the numpad, plus X / C / B by default)
- P: pause · M: mute everything · F: fullscreen · G: toggle landing ring
- Separate Music / SFX + voices / Crowd volume sliders on the title and pause screens (saved in your browser). Sound starts after your first click or key press
- Timing and contact decide shot quality (Perfect / Good / Early / Late)
- Net kill: Smash (K / . / touch Smash) near the net on a loose net shot that hangs above the tape. Timing matters: late or low goes into the net, early or too hard goes long. Tight net shots below the tape can't be killed
- Drop/Net (L) on a floater at the net plays a softer push kill
- Realistic shuttle flight: one physics model for every shot (gravity + air drag, terminal speed ~7.8 m/s)
- Bigger, flashier smashes the better you time them. A Perfect jump smash gets the full show
- 1-player (Easy / Normal / Hard) or 2-player on one keyboard; touch buttons on mobile

## Play online (1 vs 1)

1. Pick **Online** on the title screen, press **Online ♥**, then **Create room**. You get a short room code.
2. Send the code, or press **Copy invite link** and send the link (`...?room=CODE` joins straight away).
3. Your friend opens the link (or picks Online → types the code → **Join**). When they're in, choose 11 or 21 and press **Start match**.

- The host plays Nailoong and the guest plays Berry. Each of you uses your own Player 1 keys (A / D, Space, J, K, L, Shift by default, or whatever you set in Controls) or touch.
- It's a direct peer-to-peer WebRTC link. A public PeerJS server is used only to find each other. Your own moves show instantly; your opponent's reach you about half your ping later (the ping is shown top-left).
- Rematch from the end screen. If someone drops, the room stays open so they can reconnect.
- Some strict networks (certain office, school or mobile setups) block peer-to-peer connections. If joining never connects, try another network. You can also add your own TURN server with `?turn=turn:host:3478,user,pass`.

## Sounds

Racket hits use a real jump-smash sound recorded on Brian's own court, embedded in the page (a short, cleaned 24 kHz clip). Perfect smashes play the full hit, good smashes a softer version, and mistimed smashes sound like a frame hit. The Nailoong and Berry voices, crowd and background music are synthesized in the browser (Web Audio). No official Nailoong audio is used.

## Feedback welcome!

Tried it? Tell Brian what felt fun, what felt off, and any bugs you spotted.

## v15.2 / v15.3 – Career, shop, challenges
- **Career**: 8-stage ladder (Doraemon → Pikachu → Naruto → Batman → Hulk → Wonder Woman → Thor → golden **Champion Nailoong**), best-of-1 early, best-of-3 from stage 5. Beating a stage unlocks that hero.
- **Coins & shop/locker**: buy characters, racket colours, headbands and court themes. Progress is stored locally (`nailoong.progress.v1`); Reset is in the shop (asks twice).
- **Challenges & records**: 21 challenges with coin rewards; records for matches, streaks, fastest smash, longest rally, net kills, specials.
- **Match options**: 11 / 15 / 21 points, 1 game or best of 3, deuce with caps (15 / 21 / 30).
- **Fun modes** (offline): Smash only, Giant shuttle, Low gravity. Doubles: not yet (TODO).
- **Game feel**: slow-mo + camera punch on big winners, instant replay (**R**, or automatic after great points – any key skips), rally counter with "Great rally!", confetti on match win.

## v15.1 – New hero art, menus, special effects, stamina
- **Hero art**: the 14 guest heroes are new cute chibi mascot renders (original fan art made for this game, generated from text descriptions in the Nailoong toy style; no studio art or logos copied), 512 px tall WebP embedded in the file.
- **Menus**: clean title screen (Play, Career, Quick Match, Online, Characters, Shop, Challenges, How to Play, Settings), a Quick Match setup screen with a **Game mode** row (Normal / Smash Only / Giant Shuttle / Low Gravity, with a description), a Settings screen (volumes, landing ring, slow-motion effects on/off, fullscreen, controls, reset progress) and a tabbed How to Play. Esc goes back on every screen.
- **Special moves** now have big effects: name banner, screen-edge glow, aura, and themed shot effects (lightning, spin glitter/web, shield dome, afterimages, wind aura, repulsor trail, milk sparkle). The online guest sees them too.
- **Slow motion** is now a short freeze-frame (60–110 ms) plus a 0.25 s ease back to full speed, offline only; can be switched off in Settings.
- **Stamina**: moving is free; every shot costs a little (jump smash 12, smash 9, net kill 7, special 10, punch 5, drop/net 4, clear/lift 2.5), lunge 5, jump 4. Gold ⚡ stamina bar and purple-pink ★ special bar under each player.
- Controls screen: "Menu keys" (pause, mute, fullscreen, landing ring, replay) and clearer reset buttons.
- Storage: `nailoong.settings.v1` (slow-motion setting).
