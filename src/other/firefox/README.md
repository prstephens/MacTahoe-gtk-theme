
## <p align="center"> <b> Firefox Safari theme </b> </p>
![01](preview.png?raw=true)
<p align="center">A MacOSX Tahoe Safari theme for Firefox 120+</p>

## Description

This is a bunch of CSS code to make Firefox look closer to MacOSX Tahoe Safari theme.
Based on https://github.com/rafaelmardojai/firefox-gnome-theme

## Installation

Run: `./tweaks.sh -f`

or you can edit the config file

Run: `./tweaks.sh -e`

### Adaptive version support now!

https://github.com/user-attachments/assets/9b99297f-e6b3-4aa0-812a-331cddb517ce

Run: `./tweaks.sh -f adaptive` to install it

You need install adaptive-tab-bar-colour plugin first. https://addons.mozilla.org/firefox/addon/adaptive-tab-bar-colour/

### Manual installation

1. Go to `about:support` in Firefox.
2. Application Basics > Profile Directory > Open Directory.
3. Copy `chrome` folder Firefox config folder.
4. If you are using Firefox 69+:
	1. Go to `about:config` in Firefox.
	2. Search for `toolkit.legacyUserProfileCustomizations.stylesheets` and set it to `true`.
5. Restart Firefox.
6. Open Firefox customization panel and:
	1. Use *Title bar* option to toggle CSD if is not set by default.
	2. Move the new tab button to headerbar.
	3. Select light or dark variants on theme switcher.
7. Be happy with your new gnomish Firefox.

## Enabling optional features
Open `userChrome.css` with a text editor and follow instructions to enable extra features. Keep in mind this file might change in future versions and your configuration will be lost. You can copy the @imports you want to enable to a new file named `customChrome` directly in your `chrome` directory if you want it to survive updates. Remember all @imports must be at the top of the file, before other statements.

## Known bugs

### CSD have sharp corners
See upstream [bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1408360).

#### Wayland fix:
1. Go to the `about:config` page
2. Search for the `layers.acceleration.force-enabled` preference and set it to true.
3. Now restart Firefox, and it should look good!

#### X11 fix:
1. Go to the `about:config` page
2. Type `mozilla.widget.use-argb-visuals`
3. Set it as a `boolean` and click on the add button
4. Now restart Firefox, and it should look good!

## Development

If you wanna mess around the styles and change something, you might find these
things useful.

To use the Inspector to debug the UI, open the developer tools (F12) on any
page, go to options, check both of those:

- Enable browser chrome and add-on debugging toolboxes
- Enable remote debugging

Now you can close those tools and press Ctrl+Alt+Shift+I to Inspect the browser
UI.
