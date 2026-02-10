# Asset Manifest

All binary assets live in the main Bambloom project repository. Clone it to access them.

## Asset Locations (in Bambloom Project)

### Mascot / Panda Images
| File | Path | Description |
|------|------|-------------|\n| Main mascot | `app/assets/mascot.png` | Primary panda image (also used as app icon) |
| Happy | `app/assets/mascot/panda_happy.png` | Pleased expression |
| Wave | `app/assets/mascot/panda_wave.png` | Friendly waving |
| Idle | `app/assets/mascot/panda_idle.png` | Neutral/waiting |
| Blink | `app/assets/mascot/panda_blink.png` | Cute blinking |
| Celebrate | `app/assets/mascot/panda_celebrate.png` | Excited celebration |

### Flower Images (Garden)
| File | Path | Type |
|------|------|------|
| Flower 1-12 | `app/assets/Flowers/Flower1.png` through `Flower12.png` | Regular flowers (random daily reward) |
| Flower 13-15 | `app/assets/Flowers/Flower13.png` through `Flower15.png` | Golden Bloom (perfect day reward) |
| Manifest | `app/assets/Flowers/flower_manifest.json` | Metadata for all flowers |

### Lottie Animations
| File | Path | Usage |
|------|------|-------|
| Safe Space | `app/assets/animations/safe_space.json` | Welcome/onboarding |
| Rest Without Guilt | `app/assets/animations/rest_without_guilt.json` | Rest day support |
| Overwhelmed to Peace | `app/assets/animations/overwhelmed_to_peace.json` | Calm/meditation |

### App Icons
| Platform | Path |
|----------|------|
| iOS (all sizes) | `app/ios/Runner/Assets.xcassets/AppIcon.appiconset/` |
| Android (all densities) | `app/android/app/src/main/res/mipmap-*/` |
| macOS | `app/macos/Runner/Assets.xcassets/AppIcon.appiconset/` |
| Web | `app/web/icons/` |
| Highest res (1024x1024) | `app/ios/Runner/Assets.xcassets/AppIcon.appiconset/Icon-App-1024x1024@1x.png` |

### Splash Screens
| Platform | Path |
|----------|------|
| Android (all densities) | `app/android/app/src/main/res/drawable-*/splash.png` |
| iOS | `app/ios/Runner/Assets.xcassets/LaunchImage.imageset/` |

### App Screenshots (for marketing)
| File | Path | Content |
|------|------|---------|
| Dashboard | `remotion/public/screenshots/dashboard.png` | Main dashboard view |
| Garden | `remotion/public/screenshots/garden.png` | Flower garden |
| Journal | `remotion/public/screenshots/journal.png` | Reflection journal |
| Reflect | `remotion/public/screenshots/reflect.png` | Reflection screen |
| Affirmations | `remotion/public/screenshots/affirmations.png` | Daily affirmation card |
| Choose Path | `remotion/public/screenshots/choose-path.png` | Journey path |
| Me/Profile | `remotion/public/screenshots/me.png` | Profile view |

### Generated App Store Screenshots
| File | Path |
|------|------|
| 1-Hero | `remotion/out/appstore/1-Hero.png` |
| 2-Garden | `remotion/out/appstore/2-Garden.png` |
| 3-Reflect | `remotion/out/appstore/3-Reflect.png` |
| 4-Progress | `remotion/out/appstore/4-Progress.png` |
| 5-ChoosePath | `remotion/out/appstore/5-ChoosePath.png` |
| 6-Habits | `remotion/out/appstore/6-Habits.png` |
| 7-Philosophy | `remotion/out/appstore/7-Philosophy.png` |

### Video Assets
| File | Path | Description |
|------|------|-------------|
| Hook video | `remotion/public/video/hook-exhausted.mp4` | Emotional hook clip |

### Remotion Copies (for video rendering)
| Asset | Path |
|-------|------|
| Flowers (all 15) | `remotion/public/assets/flowers/` |
| Mascot variations | `remotion/public/mascot/` |

## Key Design Tokens

- **Launch screen background:** `#EFECE8`
- **App icon source:** `app/assets/mascot.png`
- **Primary font:** Quicksand (Google Fonts)
- **Secondary font:** Inter (Google Fonts)
