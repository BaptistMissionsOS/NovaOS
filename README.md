<img height="55" src="https://github.com/user-attachments/assets/928feace-3086-413a-8376-2f131c3e2f91"/>

# NovaOS
The vanilla JavaScript operating system for the web. Because Web Apps can run without the cloud sign-in.  

```txt
Version: 2.1
Title: Lazarus
```
[Homepage](https://runnova.github.io/) &bull; [Docs](https://novaos.gitbook.io/novaos-docs) &bull; [Discord](https://discord.gg/atkqbwEQU8)

> **In this document:** <br>
> About &bull; In 30 seconds &bull; Key features &bull; Run it &bull; Self Hosting NovaOS &bull; Resources &bull; Making NovaOS Apps

<img width="1606" height="910" alt="image" src="https://github.com/user-attachments/assets/220c70a7-158d-4795-af47-69c8ca485f0a" />

<h1>About</h1>

- NovaOS is a fully offline, GPLv3 web desktop that runs entirely in your browser. 
- NovaOS exists for user privacy, self-hostable and with no cloud dependency. Your data stays on your device, what NovaOS apps can know is what you give them.
- You can initialize and boot into your NovaOS web desktop within 5 seconds on an average modern device (if self-hosted).
- Nova Ecosystem is a collection of features, including apps, themes, permission systems, and styling standards.

## In 30 seconds
Here's few examples on what you can do within 30 seconds within NovaOS on a fresh device:
- Create a fresh local NovaOS account with all default apps and settings.
- Create files, folders and configure settings in NovaOS files and settings apps.
- Install even more apps from the built-in store app.
- Install and run multiple NovaOS panel widgets.
- Build apps in a local environment with a full virtual file system.

## Key features
- NovaOS is **mobile friendly**, **fully local** **web desktop** packaged as a progressive web application.
- NovaOS is **Open-Source** under GPL v3.
- It has a codebase built entirely on pure **HTML, vanilla JavaScript, and CSS** making it very reliable and private, as it can function fully offline, thanks to its local-first nature.
- NovaOS lets you encrypt all your imported files by a password, locally without storing the password anywhere.
- A suite of default applications to ease your work. There's also a store where you can install even more applications!
- NovaOS is designed for stability and control while having customizability and a wide support. Maintaining simplicity and efficiency in UI. No flashy effects or extensive animations.

## Live version - try it now
GitHub Pages: [https://runnova.github.io/NovaOS/](https://runnova.github.io/NovaOS/).
> [!NOTE]
> If you are on a mobile, NovaOS Mobile Mode works really well as a PWA. Learn How To Install [here](https://novaos.gitbook.io/main/get-started/access-novaos#installing-novaos-as-an-app-in-chrome).

## Self hosting NovaOS locally
1. Clone the repository
```sh
git clone https://github.com/runnova/NovaOS.git
cd NovaOS
```
2. Start a local server (you can use anything like NodeJS, Nginx or python as it works on any static server)
```sh
python -m http.server 8000
```
3. Your NovaOS would be live on http://localhost:8000.

# Resources
- Read the documentation and help, [here](https://novaos.gitbook.io/main).
- NovaOS videos on our [Youtube Playlist](https://www.youtube.com/watch?v=o3Xr6DHxcFo&list=PLVY7raF48Kj5cBsNIvvta5dTCleSSgQa-).

## Making NovaOS Apps
Web development has never been this powerful. Find out more about NovaOS app development. Here are some resources to help you do it:
- [Documentation](https://novaos.gitbook.io/main)
- [Discord server](https://discord.gg/atkqbwEQU8)

## Be first to know 
Join the [Discord server](https://discord.gg/atkqbwEQU8) for news, polls, ideas, issues, or being a part of developing NovaOS. You can also find me there!

> If you're wondering, NovaOS repository was recently moved here from adthoughtsglobal/Nova-OS.


## No external
Summary
All external dependencies have been successfully localized:

Assets Downloaded:

Folder	Files
assets/js/	ace.min.js, jquery-3.1.1.min.js, jquery-3.6.4.min.js, semantic-ui.min.js, js-beautify.min.js, color-thief.umd.js, jsmediatags.min.js, interact.min.js, jscolor.js
css	semantic-ui.min.css, ace.min.css, fonts-local.css (+ font-specific CSS files)
fonts	Poppins, Inconsolata, Material Icons, Material Symbols, Sono, DM Sans, Xanh Mono
json	mime-db.json, store-v2.json, themes.json, visualizerDB.json, rotur-info.json, rotur-badges.json
images	cameraSample.png
visualizers	blobs.js, classic.js, disc.js, fluid.js, fractal.js, lines.js, waveform.js
store	Empty directory for app installations
Files Updated:

index.html, bios.html, nova.css
appdata/studio.html, musicplr.html, text.html, gallery.html, liza.html, time.html, files.html, settings.html, camera.html, store.html
scripties.js
roturstyle.css
sw.js
Self-hosting complete - NovaOS now runs with zero external CDN dependencies. All resources served from local assets folder.

These external dependencies that will break when offline:

## **Will Break Offline:**

| File | External URL | Purpose |
|------|-------------|---------|
| [liza.html](cci:7://file:///NovaOS/appdata/liza.html:0:0-0:0) | `en.wikipedia.org/w/api.php` | Wikipedia API for chat |
| [liza.html](cci:7://file:///NovaOS/appdata/liza.html:0:0-0:0) | `raw.githubusercontent.com/LDNOOBW/.../en` | Profanity filter word list |
| [rotur.js](cci:7://file:///NovaOS/scripts/rotur.js:0:0-0:0) | `social.rotur.dev/claim_daily` | Daily credit API call |

## **Now Available Offline:**

### Store App

| File | Previous URL | Local Path |
|------|--------------|------------|
| store.html | `adthoughtsglobal.github.io/Nova-Store/db/v2.json` | `../assets/json/store-v2.json` |
| store.html | `adthoughtsglobal.github.io/Nova-Store/db/themes.json` | `../assets/json/themes.json` |
| store.html | `adthoughtsglobal.github.io/` | `../assets/store/` |

### Music Player

| File | Previous URL | Local Path |
|------|--------------|------------|
| musicplr.html | `novaos-web.github.io/plr/visualizerDB.json` | `../assets/json/visualizerDB.json` |
| musicplr.html | `novaos-web.github.io/plr/visualizers/*.js` | `../assets/js/visualizers/*.js` |

### Rotur Integration

| File | Previous URL | Local Path |
|------|--------------|------------|
| rotur.js | `raw.githubusercontent.com/Mistium/Origin-OS/.../info.json` | `../assets/json/rotur-info.json` |
| rotur.js | `raw.githubusercontent.com/RoturTW/Badges/.../badges.json` | `../assets/json/rotur-badges.json` |

### Files App

| File | Previous URL | Local Path |
|------|--------------|------------|
| files.html | `unpkg.com/interactjs/dist/interact.min.js` | `../assets/js/interact.min.js` |

### Studio App

| File | Previous URL | Local Path |
|------|--------------|------------|
| studio.html | `http://127.0.0.1:8000/assets/css/fonts-local.css` | `../assets/css/fonts-local.css` |
| studio.html | `http://127.0.0.1:8000/assets/css/semantic-ui.min.css` | `../assets/css/semantic-ui.min.css` |
| studio.html | `http://127.0.0.1:8000/assets/css/ace.min.css` | `../assets/css/ace.min.css` |
| studio.html | `http://127.0.0.1:8000/assets/js/js-beautify.min.js` | `../assets/js/js-beautify.min.js` |
| studio.html | `http://127.0.0.1:8000/assets/js/jquery-3.1.1.min.js` | `../assets/js/jquery-3.1.1.min.js` |
| studio.html | `http://127.0.0.1:8000/assets/js/semantic-ui.min.js` | `../assets/js/semantic-ui.min.js` |
| studio.html | `http://127.0.0.1:8000/assets/js/ace.min.js` | `../assets/js/ace.min.js` |

### Settings App

| File | Previous URL | Local Path |
|------|--------------|------------|
| settings.html | `code.jquery.com/jquery-3.6.4.min.js` | `../assets/js/jquery-3.6.4.min.js` |
| settings.html | `jscolor.com/release/2.5/jscolor-2.5.2/jscolor.js` | `../assets/js/jscolor.js` |

### Camera App

| File | Previous URL | Local Path |
|------|--------------|------------|
| camera.html | `runnova.github.io/cameraSample.png` | `../assets/images/cameraSample.png` |

### Downloaded Assets

| Location | Files |
|----------|-------|
| `assets/json/` | store-v2.json, themes.json, visualizerDB.json, rotur-info.json, rotur-badges.json |
| `assets/js/` | interact.min.js, jquery-3.6.4.min.js, jscolor.js |
| `assets/js/visualizers/` | blobs.js, classic.js, disc.js, fluid.js, fractal.js, lines.js, waveform.js |
| `assets/images/` | cameraSample.png |
| `assets/store/` | Empty directory for app installations |