# Slopeward – Dachschrägen-Planer

Android-App zum Planen von Schränken unter der Dachschräge. Du gibst die Höhe am Kniestock, die Höhe am höchsten Punkt und den waagerechten Abstand dazwischen ein. Die App rechnet daraus die Neigung, eine Zuschnittliste und die Schnittwinkel.

Zwei Einbauarten:
- **An der Giebelwand**: Die Schräge läuft über die Breite des Schranks, die Türen werden Trapeze.
- **Vor dem Kniestock**: Die Schräge läuft über die Tiefe, die Seitenteile werden Trapeze.

Die App läuft offline und merkt sich deine Eingaben. „Liste kopieren“ legt die Zuschnittliste in die Zwischenablage.

## APK herunterladen

GitHub baut die App nach jeder Änderung automatisch.

1. Oben auf **Actions** gehen und den neuesten Lauf mit grünem Haken öffnen.
2. Ganz unten bei **Artifacts** auf **Dachschraege-APK** klicken und die ZIP entpacken.
3. `app-debug.apk` aufs Handy kopieren und antippen. Beim ersten Mal „Unbekannte Apps installieren“ erlauben.

Die Artifacts bleiben 90 Tage liegen. Danach unter Actions → „APK bauen“ → **Run workflow** einen neuen Build starten.

Bei einem Update die neue APK einfach drüber installieren. Deine Eingaben bleiben dabei erhalten.

## Aufbau

| Pfad | Inhalt |
|---|---|
| `app/src/main/assets/index.html` | Der ganze Planer: Oberfläche und Rechenlogik |
| `app/src/main/java/.../MainActivity.java` | Zeigt die Seite an und kümmert sich um die Zwischenablage |
| `.github/workflows/build-apk.yml` | Baut die APK auf GitHub |

Änderungen am Planer passieren fast immer nur in `index.html`.

## Selbst bauen (optional)

Mit Android Studio: Ordner öffnen, dann **Build → Build App Bundle(s)/APK(s) → Build APK(s)**. Die APK liegt danach unter `app/build/outputs/apk/debug/`.
