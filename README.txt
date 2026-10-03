Holography Bench - installable web app (PWA)
=============================================

WHAT IS IN THIS FOLDER
  index.html            the simulator (WebGPU + CPU fallback, GPU check at start-up)
  manifest.webmanifest  app name, icons and colours (makes it installable)
  sw.js                 service worker (keeps the app working offline after the first visit)
  icons/                app icons

An installable web app must be served from an https:// address. Opening index.html
by double-click still works, but then it cannot be installed.

PUT IT ON GITHUB PAGES (free, about 10 minutes, no programming)
  1. Sign in at https://github.com (create a free account if needed).
  2. Click "+" (top right) -> "New repository".
     Name: holography-bench   Visibility: Public   -> "Create repository".
  3. On the new page click "uploading an existing file".
     Drag in index.html, manifest.webmanifest, sw.js AND the icons folder
     (the contents of this folder, not the folder itself) -> "Commit changes".
  4. Open Settings -> Pages. Under "Build and deployment":
     Source = "Deploy from a branch", Branch = "main", folder = "/ (root)" -> Save.
  5. Wait 1-3 minutes and refresh that Pages screen. It shows your address:
        https://YOUR-USERNAME.github.io/holography-bench/

INSTALL IT
  Windows / Mac / Linux (Chrome or Edge): open the address, then click the
  "Install app" button in the page header, or the install icon at the right
  end of the address bar. It gets its own window and a Start-menu/Dock entry.
  Android (Chrome): menu -> "Install app" / "Add to Home screen".
  iPhone / iPad (Safari): Share -> "Add to Home Screen". WebGPU on iOS depends
  on the iOS version; the GPU check will tell you, and the CPU fallback works.

UPDATING LATER
  Upload the changed files to the same repository, and change the VERSION line
  at the top of sw.js (e.g. holobench-v1.0.1). Installed copies show
  "Update ready: reload" the next time they are opened online.

PRIVACY
  Everything runs in the browser; nothing is sent anywhere. Note that a Public
  repository means anyone with the address can open the simulator.
