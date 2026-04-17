                                  Threat Management Dashboard

This is a lightweight, front-end-only dashboard that simulates how a basic threat management system might work. It’s designed mainly for demonstration and learning purposes, so everything runs directly in the browser—no backend or external services involved.

Preview:
https://via.placeholder.com/800x400?text=Threat+Management+Dashboard

Overview

The dashboard is split into three simple categories:

* Ransomware
* Virus
* Remote Access / SSL

Each category contains a small list of files representing simulated threats. You can interact with them just like you would in a real system—download, add, remove, and review.

The idea here is not to build a real antivirus tool, but to show how such a system could look and behave from a UI perspective.

Main Features

File interaction
Clicking on any file will download a harmless .txt file and open a modal that walks through a basic “infection” scenario. It includes a progress bar and a few steps just to make it feel realistic.

Adding files
You can add files in two ways:

* Use the “Add file” option inside a category
* Use the global “Upload file” button

The dashboard will keep the original file name and size, but it doesn’t read or process the file itself.

Removing files
Each file row has a delete (trash) icon. Once removed, the UI updates immediately, including the totals.

View all
Each category has a “View all” option that opens a modal with the full list of files. From there, you can download or delete items individually.

Live stats
There’s a small metrics section that keeps track of:

* total number of files
* combined size
* last updated time

These update automatically whenever something changes.

How it works

Everything is handled on the client side using plain JavaScript. There’s no database or server—data is just stored in memory while the page is open.

The entire project is contained in a single HTML file with:

* embedded CSS for styling
* embedded JS for logic and state
* a few inline SVGs for icons

You can just open it in a browser and it works.

Example data

The dashboard starts with a few placeholder files:

* ransom_payload.txt (2.4 MB)
* virus_sample.txt (1.1 MB)
* rat_tool.txt (3.8 MB)

These are just simple text files with dummy content.

Safety note

All downloads are plain text files and don’t do anything harmful. Even if you upload something like an executable, the app doesn’t inspect or run it—it only displays the name and size.

Nothing is uploaded anywhere, and no data leaves your browser.

Customisation

If you want to tweak things:

* File descriptions can be changed in the JavaScript (look for the description map)
* Categories can be extended by adding to the category arrays
* Styles (colors, icons, etc.) are easy to adjust in the CSS

You could also hook this up to localStorage if you want basic persistence between sessions.

Final note

This project is mainly meant as a UI/UX demo rather than a real security tool. It’s useful if you want to showcase front-end skills or experiment with dashboard-style layouts.
