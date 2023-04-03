# 06 Build & Deploy
Um das Projekt auf einen Webserver zu laden, müssen wir den Code kompilieren.

## 1) Build
Um dein Projekt zu kompilieren, führe folgenden Befehl aus:

```
npm run build
```

Im Ordner `dist` in deinem Projektordner findest du nun das kompilierte Projekt, welches wir auf den Webserver laden wollen.

## 2) Projekt hochladen
Lade den gesamten Inhalt des Ordners `dist` nun auf einen Webserver deiner Wahl hoch. Verwende dafür beispielsweise [Filezilla](https://filezilla-project.org).

## 3) Serverkonfiguration
>When using history mode, the URL will look "normal," e.g. `http://oursite.com/user/id`. Beautiful!

>Here comes a problem, though: Since our app is a single page client side app, without a proper server configuration, the users will get a 404 error if they access `http://oursite.com/user/id` directly in their browser. Now that's ugly.

Erstelle eine Konfigurationsdatei namens `.htaccess` und lege sie im Ordner `web` des Servers ab. Nun funktioniert das Routing.

.htaccess
```
<IfModule mod_rewrite.c>
  RewriteEngine On
  RewriteBase /
  RewriteRule ^index\.html$ - [L]
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_FILENAME} !-d
  RewriteRule . /index.html [L]
</IfModule>
```

[Dokumentation Vue Router](https://v3.router.vuejs.org/guide/essentials/history-mode.html#example-server-configurations)

# Navigation

👆 [Zurück zur Übersicht](https://github.com/Witzelfitz/MMA20/tree/main/vuejs)
