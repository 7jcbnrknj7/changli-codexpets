[简体中文](README.md) | [日本語](README.ja.md) | [English](README.en.md)

# 长离 · Changli

## v2.0.0 — Thoughtful and gentle edition

The display name is “长离”; v2 is the asset version. The previous pet remains in the pet list as “长离v1”.

Pink hair, golden eyes, red markings on the left arm from the elbow to every fingertip, bows on both sleeves, and a cloak with a black exterior and red lining.

### Changes in this edition

- Removed playful winks, loud laughter, and jumps off the ground.
- Added writing with pen and paper, a carrier pigeon resting on her head, folding and handing over a letter, and the pigeon spreading its wings.
- Added turning with an umbrella and smiling over her shoulder, and a gentle invitation with an open, five-fingered hand.
- Added calm breathing, touching her hair, and quiet contemplation.
- Retained sixteen natural gaze directions and adjusted character sizing across actions.

![Action preview](previews/all-states.gif)

![Continuous letter-delivery demonstration](previews/letter-story.gif)

![Action keyframes](previews/motion-stills.png)

[MP4 preview](previews/all-states.mp4) · [Umbrella transition](previews/idle-umbrella-idle.gif) · [Gaze loop](previews/look-loop.gif)

## Files

| File | Contents |
| --- | --- |
| `spritesheet.png` | Final transparent sprite sheet |
| `pet.json` | Portable asset description and frame layout, using this repository's custom metadata format |
| `previews/` | Animations and keyframes |
| `CHANGELOG.md` | Version changes |
| `GITHUB_GUIDE.md` | Uploading, backing up the previous edition, branching, committing, and merging |
| `SHA256SUMS.txt` | Sprite-sheet checksum |

No account pet ID, activation state, local paths, upload sessions, or temporary download URLs are included. Uploading to GitHub does not install the pet automatically; use the sprite sheet when creating it. `pet.json` is not an official automatic-installation configuration and does not control trigger intervals.

## Layout

Transparent RGBA PNG, 1536 × 2288 px, 8 columns × 11 rows, 192 × 208 px per cell; 73 valid frames and 15 blank cells. Rows are numbered from 0.

| Row | Player state | Action in this edition | Frames |
| --- | --- | --- | ---: |
| 0 | idle | Calm idle | 6 |
| 1 | running-right | Move right | 8 |
| 2 | running-left | Move left | 8 |
| 3 | waving | Reach out to invite contact | 4 |
| 4 | jumping | Turn with umbrella and glance back, without jumping | 5 |
| 5 | failed | Quiet contemplation | 8 |
| 6 | waiting | Pigeon lands on head; waiting | 6 |
| 7 | running | Write a letter | 6 |
| 8 | review | Fold and hand over letter; pigeon spreads wings | 6 |
| 9 | look | 000°–157.5° | 8 |
| 10 | look | 180°–337.5° | 8 |

Gaze directions follow screen coordinates clockwise: 000° up, 090° right, 180° down, and 270° left.

The player decides state transitions, so actual use does not guarantee a complete letter-delivery story every time. The continuous demonstration combines states in story order. During departure, the pigeon spreads its wings and takes off above the raised hand, but does not leave the frame.

## Asset notes

The user supplied the character reference; action assets were generated and organized with AI assistance. No open-source license is attached to this package, and it does not claim ownership of the original character. Publication and reuse must comply with permissions from the relevant rights holders.
