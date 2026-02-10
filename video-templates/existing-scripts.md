# Existing Remotion Video Scripts

These are the video templates already built in the Bambloom project's Remotion setup at `remotion/src/`.

## Video 1: "I Failed 75 Hard" (15.2 seconds / 456 frames @ 30fps)

### Scene Breakdown

| Scene | Duration | Visual | Text |
|-------|----------|--------|------|
| 1. Hook | 2.5s (75f) | Dark brown gradient, scale animation | "I FAILED 75 Hard" (red) / "3 times. Back to back." |
| 2. Pain | 2.2s (65f) | Darker gradient, slide-in | "Miss ONE day?" / "Start completely over" (strikethrough) |
| 3. Pivot | 2.2s (65f) | Warm gradient, green glow, sparkles | "Then I found 75 Soft ✨" |
| 4. App Reveal | 3.5s (105f) | Cream bg, iPhone frame + dashboard | Floating badges: 💧 3L Water, 🏃 45 Min, 📖 Read 10pg |
| 5. Garden | 3.0s (90f) | Green gradient, iPhone + garden | "Your progress grows a garden 🌸" + floating flowers |
| 6. CTA | 4.0s (120f) | Panda floating, green button | "Bambloom 🎋" / "Download Free on iOS" / "Progress over perfection" |

### Transitions
- Scene 1→2: Fade
- Scene 2→3: Fade
- Scene 3→4: Slide from bottom
- Scene 4→5: Slide from right
- Scene 5→6: Fade

---

## Video 2: "75 Hard vs 75 Soft" (16.7 seconds / 501 frames @ 30fps)

### Scene Breakdown

| Scene | Duration | Visual | Text |
|-------|----------|--------|------|
| 1. Hook | 2.5s (75f) | Very dark, pulsing red glow | "75 Hard broke me." / "3 times. Back to back." |
| 2. Comparison | 4.0s (120f) | Split screen red/green | Side-by-side rules (see below) |
| 3. Pivot | 2.7s (80f) | Dark→warm transition | "Not anymore." / "I found 75 Soft 🌱" |
| 4. App Reveal | 3.3s (100f) | Cream gradient, iPhone frame | "So I built an app for it" + 4 feature badges |
| 5. Garden | 2.7s (80f) | Green gradient, flowers animate | "Your progress grows a garden" + 7 flowers |
| 6. CTA | 3.7s (110f) | Panda floating, feature list | "Bambloom 🎋" + ✅ No restart / 🍕 Cheat meals OK / 😴 Rest days / 💚 Progress > Perfection |

### Comparison Scene Details (Scene 2)

| 75 Hard (Red/Left) | 75 Soft (Green/Right) |
|--------------------|-----------------------|
| ❌ 2 workouts/day | ✅ 45 min workout |
| ❌ Strict diet, 0 alcohol | ✅ Eat well, stay mindful |
| ❌ No cheat meals ever | ✅ Cheat meals are OK! |
| 📖 Read 10 pages | 📖 Read 10 pages |
| 💧 1 gallon water | 💧 3L water |
| 💀 Miss a day? START OVER | 💚 Miss a day? Keep going |

---

## App Store Screenshots (Still Images, 1290x2796)

7 screenshots built as Remotion compositions:

1. **Hero** — Dashboard with tasks, panda, progress stats
2. **Garden** — Flower garden visualization
3. **Reflect** — Journal/reflection screen
4. **Progress** — Analytics and progress stats
5. **Choose Path** — Journey path visualization
6. **Habits** — Core habit tracker view
7. **Philosophy** — Brand messaging screen

Each also has an animated version (90-120 frames) for app previews.

---

## Technical Setup

- **Framework:** Remotion (React/TypeScript)
- **Dimensions:** 1080x1920 (TikTok 9:16)
- **Frame Rate:** 30fps
- **Fonts:** Quicksand (400, 600, 700), Inter (400, 500, 600, 700) via @remotion/google-fonts
- **Colors:** Warm Earth palette as default
- **Components:** IPhoneFrame, TextOverlay, GradientBackground, BambloomBranding
- **Assets in:** `remotion/public/` (screenshots, mascot, flowers, video clips)

## Rendering

```bash
cd remotion/
npx remotion render src/index.ts TikTokVideo1 out/tiktok-1.mp4
npx remotion render src/index.ts TikTokVideo2 out/tiktok-2.mp4
npx remotion still src/index.ts Screenshot1Hero out/appstore/1-Hero.png
```
