<h1>Custom Firefox Bookmarks Toolbar</h1>
<p>A simple guide and userChrome.css template for customizing your Firefox bookmarks toolbar.</p>
<ul>
  <li>Add custom icons to bookmark folders</li>
  <li>Show icons only or icons with text labels</li>
  <li>Adjust icon sizes and spacing</li>
  <li>Enable multi-row bookmarks toolbar</li>
  <li>Auto-hide toolbar (shows on hover)</li>
</ul>

<a href="https://github.com/giulihejt/firefox-custom-bookmark-icons/releases/latest/download/userChrome.css">
  <strong>⬇️ Download userChrome.css</strong>
</a>

<h2>Setup Instructions</h2>
<ol>
  <li>In the Firefox address bar, go to:
    <pre><code>about:config</code></pre>
    Search for:
    <pre><code>toolkit.legacyUserProfileCustomizations.stylesheets</code></pre>
    Set it to <b>true</b>.
  </li>
  <br>
  
  <li>In the address bar, go to:
    <pre><code>about:support</code></pre>
    Under <b>Application Basics</b>, find <b>Profile Folder → Open Folder</b>. The path should be:
    <pre><code>%APPDATA%\Mozilla\Firefox\Profiles\[your-profile-folder]</code></pre>
  </li>
  
  <li>Open your Profile Folder and create the following folders:
    <pre><code>chrome/
└── icons/</code></pre>
  </li>
  
  <li>Import your icon images into the <code>icons</code> folder, if customizing icons.
    <ul>
      <li>Use clear, short names.</li>
      <li>Recommended icon sizes:
        <ul>
          <li><b>16x16</b> - Standard display size.</li>
          <li><b>32x32</b> - Best for high-DPI displays.</li>
          <li><b>64x64</b> - Maximum useful size for scalability.</li>
        </ul>
      </li>
      <li>Recommended image file formats:
        <ul>
          <li><b>SVG</b> - Best choice (scalable, sharp at any size, small file size).</li>
          <li><b>PNG</b> - Good for raster images (use 32x32px or larger, then let CSS scale down).</li>
        </ul>
      </li>
    </ul>
  </li>
  <br>
  
  <li>Download the attached <code>userChrome.css</code> file (or create your own) and copy it into the <code>chrome</code> folder. Your folder structure should look like this:
    <pre><code>firefox-profile/
└── chrome/
    ├── userChrome.css
    └── icons/
        ├── tools.svg
        ├── projects.png
        └── games.svg</code></pre>
  </li>

  <li>Review the optional customizations in the file. To disable a style, either delete it or comment it out by wrapping it in <code>/* */</code>. Keep and modify the ones you want to apply.</li>
  <br>
  
  <li>Update bookmark labels and URLs in the CSS to match your folder and icon names.
    <ul>
      <li>The <code>.bookmark-item</code> label should match the name of your bookmark folder.</li>
      <li>The <code>list-style: url</code> path should lead to the icon image file you would like to pair with the bookmark.</li>
      <li>The format should look like:</li>
    </ul>
    <pre><code>.bookmark-item[label=<b>"Tools"</b>] {  list-style: url("./icons/<b>tools.svg</b>") !important; }
.bookmark-item[label=<b>"Projects"</b>] {  list-style: url("./icons/<b>project.png</b>") !important; }
.bookmark-item[label=<b>"Games"</b>] {  list-style: url("./icons/<b>games.svg</b>") !important; }</code></pre>
  </li>
  
  <li>Save your changes to <code>userChrome.css</code> and restart Firefox to apply the changes!</li>
</ol>
</p>
<p><em>Right-click → Save Link As if your browser tries to open it</em></p>

<h3>Step 2: Install</h3>
<ol>
  <li>Enable custom stylesheets in Firefox...</li>
</ol>
