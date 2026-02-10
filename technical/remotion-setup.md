# Remotion Video Framework Setup

## Overview

The Bambloom project uses [Remotion](https://www.remotion.dev/) (React/TypeScript) for programmatically generating marketing videos and App Store screenshots.

**Location:** `remotion/` directory in the main Bambloom project.

## Project Structure

```
remotion/
├── src/
│   ├── index.ts                    # Entry point, composition registry
│   ├── tiktok/
│   │   ├── TikTokVideo1.tsx        # "I Failed 75 Hard" (15.2s)
│   │   └── TikTokVideo2.tsx        # "75 Hard vs 75 Soft" (16.7s)
│   ├── screenshots/
│   │   ├── Screenshot1Hero.tsx
│   │   ├── Screenshot2Garden.tsx
│   │   ├── Screenshot3Reflect.tsx
│   │   ├── Screenshot4Progress.tsx
│   │   ├── Screenshot5ChoosePath.tsx
│   │   ├── Screenshot6Habits.tsx
│   │   └── Screenshot7Philosophy.tsx
│   └── components/
│       ├── IPhoneFrame.tsx          # Device mockup frame
│       ├── TextOverlay.tsx          # Text overlay component
│       ├── GradientBackground.tsx   # Gradient utilities
│       └── BambloomBranding.tsx     # Logo/branding component
├── public/
│   ├── assets/flowers/             # Flower PNGs (copied from app)
│   ├── mascot/                     # Panda PNGs (copied from app)
│   ├── screenshots/                # App screen captures
│   └── video/                      # Video clips (hook-exhausted.mp4)
├── out/
│   └── appstore/                   # Generated screenshots
├── package.json
└── tsconfig.json
```

## Video Specifications

### TikTok Videos
- **Width:** 1080px
- **Height:** 1920px
- **Aspect Ratio:** 9:16
- **Frame Rate:** 30fps

### App Store Screenshots
- **Width:** 1290px (iPhone 6.7")
- **Height:** 2796px

## Fonts

Loaded via `@remotion/google-fonts`:

```typescript
import { loadFont as loadQuicksand } from "@remotion/google-fonts/Quicksand";
import { loadFont as loadInter } from "@remotion/google-fonts/Inter";

loadQuicksand(); // weights: 400, 600, 700
loadInter();     // weights: 400, 500, 600, 700
```

## Color Constants (used in Remotion)

```typescript
// Brand colors
const PRIMARY_BROWN = "#6B4440";
const CREAM = "#F5EDE8";
const WARM_BEIGE = "#E8DDD5";
const SAGE_GREEN = "#7A9B6D";
const DARK_GREEN = "#5A7A50";
const SUCCESS_GREEN = "#81C784";
const GOLD = "#FFD700";

// Dramatic (for hooks)
const DARK_BROWN = "#2D1F1A";
const RED_ACCENT = "#FF6B6B";

// Gradients
const CREAM_GRADIENT = ["#F5EDE8", "#E8DDD5", "#DCD0C6"];
const DARK_GRADIENT = ["#44332F", "#2D1F1A"];
const GREEN_GRADIENT = ["#7A9B6D", "#5A7A50"];
```

## Common Animation Patterns

### Scale entrance
```typescript
const scale = interpolate(frame, [startFrame, startFrame + 15], [0, 1], {
  extrapolateRight: "clamp",
});
```

### Fade in
```typescript
const opacity = interpolate(frame, [startFrame, startFrame + 10], [0, 1], {
  extrapolateRight: "clamp",
});
```

### Floating bob (for panda)
```typescript
const float = Math.sin(frame / 15) * 8; // 8px amplitude
```

### Staggered entry (for lists)
```typescript
items.map((item, index) => {
  const delay = index * 8; // 8 frames between each
  const itemOpacity = interpolate(frame, [startFrame + delay, startFrame + delay + 10], [0, 1]);
  const slideX = interpolate(frame, [startFrame + delay, startFrame + delay + 12], [50, 0]);
});
```

## Commands

```bash
# Install dependencies
cd remotion && npm install

# Preview in browser
npx remotion preview

# Render TikTok video
npx remotion render src/index.ts TikTokVideo1 out/tiktok-1.mp4

# Render still screenshot
npx remotion still src/index.ts Screenshot1Hero out/appstore/1-Hero.png

# Render all compositions
npx remotion render src/index.ts
```

## Adding New Videos

1. Create a new `.tsx` file in `src/tiktok/`
2. Define scenes as frame ranges
3. Use existing components (IPhoneFrame, GradientBackground, etc.)
4. Register composition in `src/index.ts`
5. Add assets to `public/` if needed
6. Render with `npx remotion render`
