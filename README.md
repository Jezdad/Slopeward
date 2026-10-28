# Slopeward – Sloped Ceiling Cabinet Planner

Android app for planning cabinets under a sloped ceiling. Enter the height at the knee wall, the height at the highest point and the horizontal distance between them. The app works out the roof pitch, a cut list and the cutting angles.

The app is available in German, English, French and Spanish. It picks your phone's language on first start, and you can switch at any time.

Two installation types:
- **Against the gable wall**: the slope runs across the cabinet's width, so the doors become trapezoids.
- **In front of the knee wall**: the slope runs across the cabinet's depth, so the side panels become trapezoids.

The app works offline and remembers your inputs. "Copy list" puts the cut list on the clipboard.

## Download

1. Open the [latest release](../../releases/latest) and download `Slopeward-<version>.apk` under **Assets**.
2. Open the file on your Android phone (Android 8 or newer).
3. The first time, allow "Install unknown apps" for the app you opened the file with.

To update, install the new APK over the old one. Your inputs are kept.

## Publishing a new version

1. Go to **Releases** → **Draft a new release**.
2. Under **Choose a tag**, enter a new version such as `v1.1.0` and select **Create new tag**.
3. Add a title and a short description of what changed, then click **Publish release**.

GitHub then builds the signed APK and attaches it to the release after a few minutes.

## Project layout

| Path | Contents |
|---|---|
| `app/src/main/assets/index.html` | The whole planner: interface, calculations and translations |
| `app/src/main/java/.../MainActivity.java` | Displays the page and handles the clipboard |
| `.github/workflows/build-apk.yml` | Builds the APK and attaches it to releases |

Changes to the planner almost always happen in `index.html` only.

## License

[Apache License 2.0](LICENSE)
