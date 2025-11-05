# Custom Firefox Bookmarks Toolbar

A simple guide and userChrome.css template for customizing your Firefox bookmarks toolbar.

- Add custom icons to bookmark folders
- Show icons only or icons with text labels
- Adjust icon sizes and spacing
- Enable multi-row bookmarks toolbar
- Auto-hide toolbar (shows on hover)

**[⬇️ Download userChrome.css](https://github.com/giulihejt/custom-firefox-bookmarks-toolbar/releases/download/v1.0.0/userChrome.css)**

**[⬇️ Download Colorful Folder Icon Set](https://github.com/giulihejt/custom-firefox-bookmarks-toolbar/releases/download/v1.0.0/colorful-folder-icon-set.zip)**

**[⬇️ Download White Minimal Icon Set](https://github.com/giulihejt/custom-firefox-bookmarks-toolbar/releases/download/v1.0.0/white-minimal-icon-set.zip)**

<details>
<summary><h3>Before/After Images</h3></summary>
Before:<br>
   <img width="950" height="471" alt="Bookmarks toolbar before." src="https://github.com/user-attachments/assets/a247e701-e117-4631-8e2d-2b0c7ee214f6" />
   
After (with labels):<br>
   <img width="950" height="215" alt="Bookmarks toolbar after, with labels." src="https://github.com/user-attachments/assets/ed3391f3-306b-44a0-846c-1942d351d2d7" />

After (without labels):<br>
   <img width="950" height="176" alt="Bookmarks toolbar after, without labels." src="https://github.com/user-attachments/assets/d9669ded-bd62-4239-8e26-3030ed5cb65a" />
</details>


<details>   
<summary><h3>Setup Instructions</h3></summary>

1. In the Firefox address bar, go to:
```
   about:config
```
   Search for:
```
   toolkit.legacyUserProfileCustomizations.stylesheets
```
   Set it to **true**.
   

2. In the address bar, go to:
```
   about:support
```
   Under **Application Basics**, find **Profile Folder → Open Folder**. The path should be:
```
   %APPDATA%\Mozilla\Firefox\Profiles\[your-profile-folder]
```

3. Open your Profile Folder and create the following folders:
```
   chrome/
   └── icons/
```

4. Import your icon images into the `icons` folder, if customizing icons.
   - Use clear, short names.
   - Recommended icon sizes:
     - **16x16** - Standard display size.
     - **32x32** - Best for high-DPI displays.
     - **64x64** - Maximum useful size for scalability.
   - Recommended image file formats:
     - **SVG** - Best choice (scalable, sharp at any size, small file size).
     - **PNG** - Good for raster images (use 32x32px or larger, then let CSS scale down).


5. Download the attached `userChrome.css` file (or create your own) and copy it into the `chrome` folder. Your folder structure should look like this:
```
   firefox-profile/
   └── chrome/
       ├── userChrome.css
       └── icons/
           ├── tools.svg
           ├── projects.png
           └── games.svg
```

6. Review the optional customizations in the file. To disable a style, either delete it or comment it out by wrapping it in `/* */`. Keep and modify the ones you want to apply.


7. Update bookmark labels and URLs in the CSS to match your folder and icon names.
   - The `.bookmark-item` label should match the name of your bookmark folder.
   - The `list-style: url` path should lead to the icon image file you would like to pair with the bookmark.
   - The format should look like:
```css
   .bookmark-item[label="Tools"] {  list-style: url("./icons/tools.svg") !important; }
   .bookmark-item[label="Projects"] {  list-style: url("./icons/project.png") !important; }
   .bookmark-item[label="Games"] {  list-style: url("./icons/games.svg") !important; }
```

8. Save your changes to `userChrome.css` and restart Firefox to apply the changes!
</details>
