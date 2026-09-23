# lancepounds.github.io

My personal site. It looks like an old desktop: a wallpaper, icons you open,
windows you drag around, and a taskbar with a start menu. Two things live on
it, a short bio and my game.

**Live at:** https://lancepounds.github.io/

## What's in here

| File | What it is |
| --- | --- |
| `index.html` | The whole site. HTML, CSS, and JavaScript in one file, no build step and nothing to install. |
| `headshot.jpg` | Optional. My photo. If it's missing, the site shows "LP" instead. |

## What's on the desktop

Three windows: **About Lance**, **Zombie Trails**, and **Speechy**. The last two
each load the real app inside the window, straight from its own repo:

- Zombie Trails, from https://lancepounds.github.io/zombie-trails/
- Speechy, from https://lancepounds.github.io/Speechy/

Nothing is copied into this repo, so whatever I push to either app shows up here
on the next reload.

## The game

Saved games live in the browser, under the `lancepounds.github.io` name. Since
both the site and the game sit there, a save made in either place is the same
save.

## Publishing

GitHub Pages serves this repo because of its name. To publish a change:

1. Edit or upload the file.
2. Commit to the `main` branch.
3. Wait a minute, then reload the site. A hard refresh
   (Ctrl+Shift+R, or Cmd+Shift+R on a Mac) clears an old cached copy.

Check **Settings → Pages** if it ever stops updating. It should say the site is
building from `main`.

## Making changes

Everything is in `index.html`.

- **Bio text:** in the `About Lance` window, near the top of the `<body>`.
- **Photo:** replace `headshot.jpg`. Anything roughly 4 by 5 works.
- **Game address:** the `GAME_URL` line at the top of the script, plus the two
  "Open in a new tab" links.
- **Speechy:** its window uses `data-src="https://lancepounds.github.io/Speechy/"`.
  Edit Speechy itself in its own repo, not here. GitHub Pages is case
  sensitive, so that capital S matters.
- **Colors and window styling:** the variables at the top of the `<style>`
  block. `--title` is the title bar, `--face` is the beige window body.
## Speechy

Speechy is built in the `Speechy` repo and opens in a window here. Two notes
carried over from it: the **Make a sentence** button needs the Claude
runtime and won't work on GitHub Pages, and saved phrases stay in one browser
rather than syncing between devices.

## Making changes, continued

- **Adding a window:** copy a whole `<section class="win">` block, give it a new
  `id`, and add that id to the `['about', 'game']` list in the script. Desktop
  icons, taskbar buttons, and start menu entries all point at a window with
  `data-open="the-id"`.

## How it behaves

- Icons take a double-click to open, or one tap on a touch screen.
- Title bars drag. The bottom-right corner resizes. Double-clicking a title bar
  maximizes.
- Minimize, maximize, and close all work, and closed windows reopen from the
  desktop, the taskbar, or the start menu.
- The start menu has Restart, which replays the boot screen, and Turn off,
  which blanks the screen until you turn it back on.
- On phones, windows open full screen and dragging is off.
- The boot screen is skipped for anyone whose system asks for reduced motion,
  and after the first load in a session.

## Notes

- Tested in current Chrome, Firefox, and Safari, on desktop and phone.
- The look is my own take on an early 2000s desktop. It uses no Microsoft
  artwork, logos, or wallpaper. The hills and icons are drawn in the file.
