# HAUNT

A Halloween projection visualiser. Point a webcam and a projector at a wall, step in front of it, and haunt it with your hands, body and music. It's one self-contained HTML file: no build step and no dependencies to install.

## Running it

1. Serve the folder locally, for example `npx serve .`, and open it in **Chrome**. Opening the file directly also works, but serving it is more reliable for camera and mic permissions.
2. Click **ENTER** and allow the camera.
3. It needs internet the first time so it can load MediaPipe (hand, face, body and person-mask models).
4. With no camera it falls back to a demo figure, and the mouse acts as your right hand.

## Scenes

**Pick a scene with your left hand** by holding the finger pose for about half a second, or use keys **1–7**.

| Left hand | Scene | What happens | Right hand |
|---|---|---|---|
| ☝ 1 finger | **BLOOD** | Blood drips down the wall and around you | ☝ bleed from the wall · ✋ gush · 🤏 smear |
| ✌ 2 fingers | **GHOST** | A smoky ghost of you follows a few steps behind, and your shadow lags | ☝ ghosts lean toward it · ✋ blow the smoke away · ✌ hold adds a ghost |
| 3 fingers | **SKULL** | A glowing particle skull sits on your head and copies your mouth. Keep your mouth open for 3 s and spiders or eyeballs pour out | 🤏 pull it off and throw it · ✋ blow it apart · ✌ chatter |
| ✋ 4 fingers | **FACES** | Faces push out of the wall, and your hands press through it | ☝ hold summons a face · ✋ make them scream · 🤏 drag a face |
| 🤘 index + pinky | **BLOOD PAINT** | Paint in blood that drips | ☝ paint · ✌ eraser · ✋ splatter |
| 🤙 pinky only | **PUMPKIN** | Carve a jack-o'-lantern and get a score | ☝ carve · ✌ lift the knife · ✋ hold to light it · 🤘 hold for the next design |
| 👌 OK sign | **SKELETON** | You become a glowing pixel skeleton | Dance moves: 🙌 blood rain · 👏 eyeballs · squat for spiders · jump for lightning |

**✊ Hold a fist** to clear the current scene. **Swipe ✌✌ with both hands** to hide or show the panel.

## Music

- Press **MIC IN**, or press **TAB AUDIO** and share a tab that's playing music. Tick **"Share audio"**; this is the most reliable option.
- Every scene reacts to the beat. The tracker locks onto the song's BPM, which appears top-left.
- **SOUND BLOOD** (key B): the blood stops dripping and instead forms mandalas, messages and spooky shapes that change on the beat. **SHAPES** (key N) switches between holding a shape for 4 beats then doing quick flips (MIX), holding every shape for 4 beats (HOLD 4), or a new shape on every beat (EVERY BEAT).
- **BEAT PUMP**: the whole picture zooms and flashes slightly on each beat.
- If it isn't catching the beat, adjust **BEAT SENS** or **AUDIO GAIN** in the panel.

## Setup on the wall

- **C** shows the camera view on the wall. Line up the mask of you with **MASK X / Y / SIZE**.
- **MIRROR** (M): turn it off if the camera sits beside the projector facing the wall.
- **SWAP HANDS** (S): use it if left and right come out backwards.
- **LEFT HAND SWITCH** (L): turn it off to stop your left hand from changing scenes.
- **F** goes fullscreen, **H** hides the panel, **G** hides the guide.

## Tweaking

All the tunable values are in the `SETTINGS` object at the top of the script in `index.html`, and each one has a comment. For example, you can change the blood messages, the shape list, ghost lag, skull size, how many faces appear, and pumpkin difficulty.
