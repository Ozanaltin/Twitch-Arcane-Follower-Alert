# Twitch Arcane Follower Alert

Arcane Mage-themed Twitch follower alert for the English channel, featuring a custom purple card, animated purple/blue lightning that races around the card edges, fast multi-strike timing, and rounded corner transitions.

## Features

- English follower alert text
- Custom Arcane follower card artwork
- Purple and blue lightning effects
- Lightning travels around the card perimeter
- Fast animation speed (current tuned version)
- Rounded corner pathing so the electricity flows around the frame instead of snapping through sharp 90° turns
- Cinzel + Rajdhani typography
- Twitch `{username}` alert variable support
- Transparent background for OBS/Twitch browser sources

---

## Preview

<p align="center">
  <img src="assets/Arcane-Follower-Purple.png" alt="Twitch Arcane Follower Alert preview" width="700">
</p>

> Static preview of the card artwork.  
> In the live Twitch alert, animated purple and blue lightning spins around the edges of the card.

---

## Files

```text
.
├── index.html
├── style.css
├── README.md
└── assets/
    └── Arcane-Follower-Purple.png
```

## Twitch setup

1. Open **Creator Dashboard → Alerts**.
2. Select your follower alert variant.
3. Enable custom HTML/CSS.
4. Copy the alert markup from `index.html` into Twitch's HTML editor. If Twitch only wants the alert body, copy the contents inside `<body>`.
5. Copy `style.css` into Twitch's CSS editor.
6. Keep the `{username}` variable unchanged.
7. Save the alert and send a test follow alert.

The HTML references the copy of the card image stored in this repository.

## Current alert text

```text
NEW FOLLOWER
{username}
The Circle grows stronger.
```

## Current visual tuning

- Alert position: `24%` from the top of the Twitch alert canvas
- Card width: `440px`
- Text block starts at `28%` from the left side of the card
- Lightning travel cycle: `0.5283s`
- Purple/blue color cycle: `5.73s`
- Lightning corner angles are softened to create a more curved perimeter flow

## Notes

The lightning color pattern is intentionally driven by separate movement and color animation timings. CSS does not provide true random number generation, but the unsynchronized cycles and per-segment delays create a randomized-looking sequence of purple and blue strikes when alerts trigger.

The card asset in `assets/Arcane-Follower-Purple.png` is included with the project so the alert does not depend solely on the original Twitch alert-asset URL.
