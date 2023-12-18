# <a href="https://sudo-self.github.io/oh-stick/">oh-stick</a>
notes by Jesse
![contract](https://github.com/sudo-self/oh-stick/assets/119916323/7d5d53ef-a8e0-456a-891c-32afc0e12f06)<hr>


How to create PWA

1. create manifest.json

2. link .json inside index.html

2. add a js service (app works offline)

4. convert with pre-cache

5. PWA

npm install --global sw-precache

sw-precache

npm install -g cli-real-favicon





// contract.png = App icon //

{
  "name": "oh-stick",
  "short_name": "oh-stick",
  "start_url": "index.html",
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

// link manifest.json inside idex.html //

<link rel="manifest" href="manifest.json">


// script.js //


if ("serviceWorker" in navigator) {
  // register service worker
  navigator.serviceWorker.register("service-worker.js");
}



// converting project to PWA with npm 
// run in terminal from the root directory of project

npm install --global sw-precache

sw-precache











//  favorite icons // 

npm install -g cli-real-favicon

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
