# Slopeward – Sloped Ceiling Cabinet Planner

Android app for planning cabinets under a sloped ceiling. Enter the height at the knee wall, the height at the highest point and the horizontal distance between them. The app works out the roof pitch, a cut list and the cutting angles.

The app's interface is in German.

Two installation types:
- **Against the gable wall**: the slope runs across the cabinet's width, so the doors become trapezoids.
- **In front of the knee wall**: the slope runs across the cabinet's depth, so the side panels become trapezoids.

The app works offline and remembers your inputs. "Liste kopieren" (copy list) puts the cut list on the clipboard.

## Download the APK

GitHub builds the app automatically after every change.

1. Go to **Actions** and open the latest run with a green check mark.
2. At the bottom, under **Artifacts**, click **Dachschraege-APK** and unzip the file.
3. Copy `app-debug.apk` to your phone and tap it. The first time, allow "Install unknown apps".

Artifacts are kept for 90 days. After that, start a new build under Actions → "APK bauen" → **Run workflow**.

To update, install the new APK over the old one. Your inputs are kept.

## Project layout

| Path | Contents |
|---|---|
| `app/src/main/assets/index.html` | The whole planner: interface and calculations |
| `app/src/main/java/.../MainActivity.java` | Displays the page and handles the clipboard |
| `.github/workflows/build-apk.yml` | Builds the APK on GitHub |

Changes to the planner almost always happen in `index.html` only.
