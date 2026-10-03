# Parishfolk playable SFX

Short mono clips, loudness-normalised (-16 LUFS, -1.5 dBTP), each as **OGG (Vorbis) + M4A (AAC)**, every file under 30 KB. Use OGG on web/Android, M4A on iOS Safari.

| File | Use | Source | Licence |
|---|---|---|---|
| `sfx_ui_tap.ogg` / `.m4a` | Any UI tap (Settings toggle) | Kenney, *UI Audio* (`click1.ogg`), https://kenney.nl/assets/ui-audio | CC0 1.0 |
| `sfx_hold_start.ogg` / `.m4a` | Café: finger down on Hold | Kenney, *Interface Sounds* (`tick_002.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_serve_cup.ogg` / `.m4a` | Café: glass set down / served | Kenney, *Impact Sounds* (`impactPlate_light_001.ogg`), https://kenney.nl/assets/impact-sounds | CC0 1.0 |
| `sfx_coin.ogg` / `.m4a` | Single coin landing (tip jar, Collect coin arrivals, stagger 40 ms, max 6) | Kenney, *Casino Audio* (`chips-collide-1.ogg`), https://kenney.nl/assets/casino-audio | CC0 1.0 |
| `sfx_coin_burst.ogg` / `.m4a` | Collect burst / tips burst | Kenney, *Casino Audio* (`chips-stack-1.ogg`), https://kenney.nl/assets/casino-audio | CC0 1.0 |
| `sfx_grade_nice.ogg` / `.m4a` | Café grade Nice | Kenney, *Interface Sounds* (`select_002.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_grade_great.ogg` / `.m4a` | Café grade Great | Kenney, *Interface Sounds* (`confirmation_001.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_grade_perfect.ogg` / `.m4a` | Café grade Perfect | Kenney, *Interface Sounds* (`confirmation_002.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_combo_up.ogg` / `.m4a` | Combo x2..x5 (pitch +2 semitones per step, playbackRate 1.0..1.26) | Kenney, *Interface Sounds* (`pluck_001.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_oops_soft.ogg` / `.m4a` | Over/under-fill (gentle, never a buzzer) | Kenney, *Interface Sounds* (`question_001.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_star_pop.ogg` / `.m4a` | Result card stars (pitch up per star) | Kenney, *Interface Sounds* (`glass_002.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_shift_done.ogg` / `.m4a` | Shift over, result card in | Kenney, *Interface Sounds* (`maximize_008.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_emote_pop.ogg` / `.m4a` | Emote bubble appears in town | Kenney, *Interface Sounds* (`pluck_002.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_door.ogg` / `.m4a` | Enter café / home | Kenney, *Interface Sounds* (`open_001.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_step_pavement.ogg` / `.m4a` | Footstep (off by default; every 2nd walk frame) | Kenney, *Impact Sounds* (`footstep_concrete_000.ogg`), https://kenney.nl/assets/impact-sounds | CC0 1.0 |
| `sfx_step_grass.ogg` / `.m4a` | Footstep on grass/park (off by default) | Kenney, *Impact Sounds* (`footstep_grass_000.ogg`), https://kenney.nl/assets/impact-sounds | CC0 1.0 |
| `sfx_pour_loop.ogg` / `.m4a` | Café: loop while Hold is down (1.6 s, loopable; fade 60 ms on release) | Original, synthesised with ffmpeg (band-passed pink noise + tremolo); see `../src/README` command | Ours (CC0-style, no attribution) |
| `sfx_steam_hiss.ogg` / `.m4a` | Café: milk steam on lattes, or idle machine hiss (quiet) | Original, synthesised with ffmpeg (filtered white noise) | Ours |

Kenney licence text: `LICENSE-kenney-CC0.txt` (CC0; credit optional, we credit "Sound: Kenney (kenney.nl)" in About anyway).

**Rules.** All sound is behind the Settings > Sound toggle (default on for the café, footsteps default off). Never play more than 3 coin sounds at once. Respect the OS silent switch on iOS (use `AudioContext` ambient category). No music in P0; a CC0 loop can come in P1.

Regenerate: `bash ../src/build_sfx.sh` (needs ffmpeg and the four Kenney zips in /tmp/kenney).

## P1 clips: FINAL (Sat 3 Oct 2026)
These replace the placeholder copies under the same names. Built by `bash ../src/build_sfx.sh`, which runs `../src/build_sfx_p1.py` for these 8. Every file is under 30 KB (largest: `sfx_rain_loop.m4a`, 21.0 KB).

Processing:
- Kenney clips: leading silence trimmed, loudnorm to −16 LUFS, peak capped at −1.5 dBFS. OGG and M4A are both encoded from the same WAV (no double lossy encode).
- `sfx_wrong_soft`: trimmed −8 dB so it sits at `sfx_oops_soft`'s level.

| File | Use | Length | Source | Licence |
|---|---|---|---|---|
| `sfx_tab.ogg` / `.m4a` | Tab change (single click) | 0.08 s | Kenney, *Interface Sounds* (`switch_002.ogg`, first click only), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_place_item.ogg` / `.m4a` | Decor placed in a room slot | 0.26 s | Kenney, *Impact Sounds* (`impactWood_light_002.ogg`), https://kenney.nl/assets/impact-sounds | CC0 1.0 |
| `sfx_moment_in.ogg` / `.m4a` | Moment card appears (soft glass chime) | 0.27 s | Kenney, *Interface Sounds* (`glass_001.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_card_flip.ogg` / `.m4a` | Uni Revision card flip | 0.42 s | Kenney, *Casino Audio* (`card-place-1.ogg`, quiet lead-in and silent tail trimmed), https://kenney.nl/assets/casino-audio | CC0 1.0 |
| `sfx_gauge_tick.ogg` / `.m4a` | Trade gauge needle tick (fire per tick; very short) | 0.04 s | Kenney, *Interface Sounds* (`tick_001.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_rain_loop.ogg` / `.m4a` | Rain ambience, loop while it rains (fade 400 ms in/out). Quiet: −30 dBFS RMS | 3.994 s loop | Ylmir, *Rain (loopable)*, OpenGameArt (`1.ogg` from "Rain OGG.zip"), https://opengameart.org/content/rain-loopable. Kenney has no rain clip | CC0 1.0 (`LICENSE-opengameart-rain-CC0.txt`) |
| `sfx_wrong_soft.ogg` / `.m4a` | Wrong item / bay (soft, low "hm?", never a buzzer) | 0.33 s | Kenney, *Interface Sounds* (`question_002.ogg`), https://kenney.nl/assets/interface-sounds | CC0 1.0 |
| `sfx_buy.ogg` / `.m4a` | Decor purchase (coin stack) | 0.37 s | Kenney, *Casino Audio* (`chips-stack-3.ogg`), https://kenney.nl/assets/casino-audio | CC0 1.0 |

**Rain loop.** The loop is 3.994 s, exactly 86 AAC frames at 22.05 kHz, with an equal-power crossfade at the seam, so both formats loop without a click or gap. Play it with the player's loop mode, not by restarting on "ended".

**Credits line for About:** "Sound: Kenney (kenney.nl) · Rain: Ylmir (OpenGameArt)". Neither is required under CC0.

**Note on P0 clips.** A few P0 clips decode up to about +1 dB over full scale (single-pass loudnorm on very short clips). They are approved and locked, so they're left as they are. If the CTO hears any clipping, apply a −2 dB gain to those few in code, or ask me to re-export them.
