# blurclean-firefox-theme
### Clean, transparent firefox theme

based on [https://github.com/manilarome/blurredfox](https://github.com/manilarome/blurredfox) and [https://github.com/not-holar/my_firefox_theme](https://github.com/not-holar/my_firefox_theme)

<p align="center"><img alt="Example look with theme" src="other/browser.png"/><br/><i>Example look of the browser</i></p>

## Notes
+ supports only native Firefox Dark Theme
+ tested on Manjaro KDE (and should work with other distros)
+ transparency makes problem with windows, you must make change in `userCrome.css`, you loose transparency but rest of theme should work :) 

## Installation

1. Open `about:config` and set this preferences to **'true'** 

+ **`toolkit.legacyUserProfileCustomizations.stylesheets`**
+ **`layers.acceleration.force-enabled`**
+ **`gfx.webrender.all`**
+ **`gfx.webrender.enabled`**
+ **`layout.css.backdrop-filter.enabled`**

2. Go to `about:profiles` and find your `Root Directory` and enter there.
3. Next step you can solve with two ways:
+ create new directory `chrome` and copy there repo content
+ open terminal, when you are in `Root Directory` use `git clone https://github.com/Filip-Sutkowy/blurclean-firefox-theme chrome`
4. Set **Dark Theme** in Firefox
5. Install **Tree Style Tab** addon
6. Copy content of `tst_theme.css` to Tree Style Tab / Preferences / Advanced / Extra style.

## Blur
You have to enable blur in compositor, where to find this option is based on your desktop environment, here is how to enable it with KDE:
+ Enable blur in System Settings / Workspace / Workspace Behavior / Deskop Effects
+ Download and enable **Force Blur** script in System Settings / Workspace / Window Management / KWin Scripts. Relogin to enable script configuration. Now add firefox in script config.
+ **Force Blur** need this two command to start working (maybe it's already fixed, check comments [here](https://store.kde.org/p/1294604/))
	+ `mkdir -p ~/.local/share/kservices5/`
	+ `cp ~/.local/share/kwin/scripts/forceblur/metadata.desktop ~/.local/share/kservices5/forceblur.desktop`
+ Now should working

## Reccomended Addons
These addons make this theme better
+ [TST Colored Tabs](https://addons.mozilla.org/en-US/firefox/addon/tst-colored-tabs) - make sure you configure this well! (like [this](other/tst_colours.png))
+ [Dark Reader](https://addons.mozilla.org/en-US/firefox/addon/darkreader) | [Dark Background and Light Text](https://addons.mozilla.org/en-US/firefox/addon/dark-background-light-text/) | [Darker Background Brighter Font](https://addons.mozilla.org/en-US/firefox/addon/darker-bg-brighter-font) or other addons which makes every page **DARK**
+ [Tabliss](https://addons.mozilla.org/en-US/firefox/addon/tabliss/) | [Momentum](https://addons.mozilla.org/en-US/firefox/addon/momentumdash) | [Speed Dial](https://addons.mozilla.org/en-US/firefox/addon/fvd-speed-dial) or other new page extension

## Uninstalling 
Just remove `chrome` folder, that's all