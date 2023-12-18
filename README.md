# <a href="https://sudo-self.github.io/oh-stick/">oh-stick</a>&nbsp;
![contract](https://github.com/sudo-self/oh-stick/assets/119916323/7d5d53ef)


How to create PWA

[Oh-Stick!](https://oh-stick.vercel.app/)

1. create manifest.json<img width="1165" alt="Screenshot 2023-12-18 at 8 08 23 AM" src="https://github.com/sudo-self/oh-stick/assets/119916323/81087a35-fcb2-4465-aa43-efee1b8a1cd5">

<img width="1020" alt="Screenshot 2023-12-18 at 8 01 11 AM" src="https://github.com/sudo-self/oh-stick/assets/119916323/85c28ac0-6797-4dca-8425-638da409cef6">

2. link .json inside index.html

2. add a js service script (app works offline)

4. convert with pre-cache

5. myscipt.js

  <code> 
if ("serviceWorker" in navigator) {
  // register service worker
  navigator.serviceWorker.register("service-worker.js");
}</code>


manifest.json
 
 {
  "name": "oh-stick",
  "short_name": "oh-stick",
  "start_url": "https://oh-stick.pages.dev/#",
  "scope": "./",
  "icons": [
    {
      "src": "contract.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "contract.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ],
  "theme_color": "#ffd31d",
  "background_color": "#333",
  "display": "standalone"
}
<br>

npm install --global sw-precache

sw-precache

TWA

APP

npm i @bubblewrap/cli

bubblewrap init --manifest https://d2563cab.oh-stick.pages.dev/manifest.json  

[ICON 512X512](https://bucket.jessejesse.com/android-chrome-512x512.png)

bubblewrap build

<img width="889" alt="Screenshot 2023-12-18 at 6 48 35 AM" src="https://github.com/sudo-self/oh-stick/assets/119916323/a2e6e9ed-626a-4e4c-9b5a-f40a88b2ec3f"><br>

## Favicon

npm install -g cli-real-favicon

contract.png = App icon


<hr>


faviconDescription.json

{
    "masterPicture": "/coontract.png",
    "iconsPath": "/",
    "design": {
        "ios": {
            "pictureAspect": "noChange",
            "assets": {
                "ios6AndPriorIcons": false,
                "ios7AndLaterIcons": false,
                "precomposedIcons": false,
                "declareOnlyDefaultIcon": true
            }
        },
        "desktopBrowser": {
            "design": "raw"
        },
        "windows": {
            "pictureAspect": "noChange",
            "backgroundColor": "#da532c",
            "onConflict": "override",
            "assets": {
                "windows80Ie10Tile": false,
                "windows10Ie11EdgeTiles": {
                    "small": false,
                    "medium": true,
                    "big": false,
                    "rectangle": false
                }
            }
        },
        "androidChrome": {
            "pictureAspect": "noChange",
            "themeColor": "#ffffff",
            "manifest": {
                "display": "standalone",
                "orientation": "notSet",
                "onConflict": "override",
                "declared": true
            },
            "assets": {
                "legacyIcon": false,
                "lowResolutionIcons": false
            }
        }
    },
    "settings": {
        "scalingAlgorithm": "Mitchell",
        "errorOnImageTooSmall": false,
        "readmeFile": false,
        "htmlCodeFile": false,
        "usePathAsIs": false
    }
}
