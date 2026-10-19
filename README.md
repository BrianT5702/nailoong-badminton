# Nailoong Badminton 🏸

A little browser badminton game starring Nailoong. No install needed: open the link and play on a laptop, phone or tablet.

## How to play

| | Move | Jump | Clear (punch / high, by timing) | Smash | Drop / Net shot |
|---|---|---|---|---|---|
| Player 1 | A / D | Space | J | K | L |
| Player 2 | ← / → | ↑ (or Numpad 0) | , or Enter (Numpad 1) | . (Numpad 2) | / (Numpad 3) |

- Lunge for far shots: Player 1 Left Shift or Q, Player 2 Right Shift or ; (Numpad 5); or double-tap a direction
- In 1-player mode you can also use the arrows with Z / X / C (or , . /)
- P: pause · M: mute everything · F: fullscreen · G: toggle landing ring
- Separate Music / SFX + voices / Crowd volume sliders on the title and pause screens (saved in your browser). Sound starts after your first click or key press
- Timing and contact decide shot quality (Perfect / Good / Early / Late)
- Net kill: Smash (K / . / touch Smash) near the net on a loose net shot that hangs above the tape. Timing matters: late or low goes into the net, early or too hard goes long. Tight net shots below the tape can't be killed
- Drop/Net (L) on a floater at the net plays a softer push kill
- Realistic shuttle flight: one physics model for every shot (gravity + air drag, terminal speed ~6.8 m/s)
- Bigger, flashier smashes the better you time them. A Perfect jump smash gets the full show
- 1-player (Easy / Normal / Hard) or 2-player on one keyboard; touch buttons on mobile

## Play online (1 vs 1)

1. Pick **Online** on the title screen, press **Online ♥**, then **Create room**. You get a short room code.
2. Send the code, or press **Copy invite link** and send the link (`...?room=CODE` joins straight away).
3. Your friend opens the link (or picks Online → types the code → **Join**). When they're in, choose 11 or 21 and press **Start match**.

- The host plays Nailoong and the guest plays Berry. Both use the Player 1 keys (A / D, Space, J, K, L, Shift) or touch.
- It's a direct peer-to-peer WebRTC link. A public PeerJS server is used only to find each other. Your own moves show instantly; your opponent's reach you about half your ping later (the ping is shown top-left).
- Rematch from the end screen. If someone drops, the room stays open so they can reconnect.
- Some strict networks (certain office, school or mobile setups) block peer-to-peer connections. If joining never connects, try another network. You can also add your own TURN server with `?turn=turn:host:3478,user,pass`.

## Sounds

All sounds are made in the browser (Web Audio): the Nailoong and Berry voices, crowd and background music are synthesized. No recorded or official clips are used.

## Feedback welcome!

Tried it? Tell Brian what felt fun, what felt off, and any bugs you spotted.
