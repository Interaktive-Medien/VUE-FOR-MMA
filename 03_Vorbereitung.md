# 03 Vorbereitung & Installation
1) Node.js & NPM
2) Vue CLI
3) Atom IDE

## Warum müssen wir so viel installieren?
Damit wir im Terminal Vue-Projekte erstellen können, müssen wir das Vue Command Line Interface (Vue CLI) auf unserem Computer installieren. Vue CLI ist eine Software-Library, die über den Node-Package-Manager (npm) installiert wird. Der Node-Package-Manager ist Teil von Node.js.

Zudem wollen wir noch Atom so vorbereiten, dass dieser .vue Dateien erkennt und den Code richtig einfärbt.

### Installationen
1) Node.js & Node Package Manager (npm)
3) Vue Command Line Interface (Vue CLI)
4) Atom IDE (Integrated Development Environment)

# Node.js & NPM
## Was ist Node.js?
> Node.js is an open source server environment that lets you run JavaScript on the Server.

- Wir installieren Node.js, damit wir den Node Package Manager nutzen können.

## Was ist npm?
>Npm is a package manager. It let's you install software (libraries, plugins, frameworks and applications). Typically this software is installed to build Node applications. Sometimes it isn't.

- Npm ist der grösste Software-Katalog der Welt
- Dieser enthält über 800.000 Code-Pakete.
- Open-Source-Entwickler nutzen npm, um Software zu teilen.
- JavaScript-Entwickler nutzen NPM, um fremde Bibliotheken in ihre Projekte einzubinden.

## Installation
**npm** wird zusammen mit **Node.js** installiert. Das bedeutet, dass wir Node.js installieren müssen, um npm auf dem Computer nutzen zu können.

Lade Node.js von der offiziellen Node.js-Website herunter:

1) https://nodejs.org/en/
2) Lade "Recommended for most Users" herunter
3) Installiere das .dmg bzw. .msi File
4) Öffne das Terminal und kontrolliere, ob die Installation erfolgreich war: `node -v && npm -v`

# Vue CLI
## Was ist Vue CLI?
>The CLI (`@vue/cli`) is a globally installed npm package and provides the `vue` command in your terminal. It provides the ability to quickly scaffold a new project via `vue create`.

## Installation
[Installations-Guide](https://cli.vuejs.org/guide/installation.html)

1) Öffne das Terminal, gib folgenden Befehl ein:

💻 Windows
```
npm install -g @vue/cli
```

🍎 Mac/Unix
```
sudo npm install -g @vue/cli
```

>🧠 Das `sudo` Keyword benötigen wir, um den Befehl auf Max/Unix mit Administrator-Rechten auszuführen.

2) Überprüfe die Installation mit dem Befehl vue --version

```
vue --version
```

# IDE für Atom
> Eine **IDE** (Integrated Development Environment) oder integrierte Entwicklungsumgebung ist Software für die Anwendungsentwicklung, die gängige Entwicklertools in einer zentralen grafischen Oberfläche vereint.

Bevor wir unser erstes Vue-Projekt erstellen, wollen wir Atom so vorbereiten, dass dieser .vue Files erkennt und unseren Code entsprechend einfärbt.

Dafür müssen wir folgende Atom-Packages installieren:

1) Öffne die Einstellungen in Atom mit `CTRL bzw. CMD + ,`
2) Klicke auf den Menüpunkt `+ Install`
3) Suche und installiere folgende Packages:
	1) `ide-vue`
	2) `atom-ide-ui`
	3) `language-vue`

4) Starte nach der Installation Atom neu

# Navigation
👉 [04 Ein Vue Projekt erstellen](04_Vue_Projekt.md)

👆 [Zurück zur Übersicht](https://github.com/Witzelfitz/MMA20/tree/main/vuejs)
