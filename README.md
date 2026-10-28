# Dachschrägen-Planer – Android-App

Die App packt den Dachschrägen-Schrankplaner in eine eigene Android-App. Sie läuft komplett offline. Deine Eingaben bleiben gespeichert, und „Liste kopieren“ legt die Zuschnittliste in die Zwischenablage.

## Weg A: Bauen lassen mit GitHub (ohne Installation)
1. Auf github.com ein neues Repository anlegen, z. B. `dachschraegen-planer`. Privat geht auch.
2. Den Inhalt dieses Ordners hochladen ("Add file" → "Upload files"). Den Ordner `.github` dabei mit hochladen.
3. Oben auf "Actions" gehen. Der Build "APK bauen" startet von selbst und dauert ca. 3–5 Minuten.
4. Den fertigen Lauf öffnen, unten unter "Artifacts" die Datei **Dachschraege-APK** laden und entpacken. Darin liegt `app-debug.apk`.

## Weg B: Android Studio
1. Android Studio installieren und den Ordner mit "Open" öffnen.
2. Falls Android Studio nach Gradle fragt, die Vorgabe übernehmen.
3. Menü Build → Build App Bundle(s)/APK(s) → Build APK(s).
4. Die APK liegt dann unter `app/build/outputs/apk/debug/app-debug.apk`.

## Aufs Handy
APK aufs Handy kopieren (Mail, Drive, USB) und antippen. Beim ersten Mal fragt Android, ob du "Unbekannte Apps installieren" erlauben willst. Das für die App bestätigen, mit der du die Datei öffnest (z. B. Dateien oder Chrome).

## Rechenlogik ändern
Alles steckt in `app/src/main/assets/index.html`. Danach einfach neu bauen.
