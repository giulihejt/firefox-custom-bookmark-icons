<h1>Firefox Custom Bookmark Icons</h1>

<p>A simple guide and userChrome.css template for customizing bookmark favicons in Firefox.<br>
  <ul>
    <li>Customize your folder icons.</li>
    <li>Replace missing or generic icons with custom images.</li>
    <li>Remove or edit the text formatting for your bookmarks.</li>
  </ul>
  </p>
<h2>Setup Instructions</h2>
<ol>
  <li>In the Firefox address bar, go to:<br>
    <pre><code>about:config</code></pre>
  </li>
  <li>Search for:<br>
    <pre><code>toolkit.legacyUserProfileCustomizations.stylesheets</code></pre>
  </li>
  <li>Set it to <strong>true</strong>.</li>
  <li>In the address bar, go to:<br>
  <pre><code>about:support</code></pre>
  </li>
  <li>Under <strong>Application Basics</strong>, find <strong>Profile Folder → Open Folder</strong>. The path should be:
    <pre><code>%APPDATA%\Mozilla\Firefox\Profiles\[your-profile-folder]</code></pre>
  </li>
  <li>Open your Profile Folder, create the following folders:<br>
  <pre><code>chrome/
└── icons/</code></pre>
  </li>
  <li>Import your icon images into the <code>icons</code> folder.
    <ul>
      <li>Use clear, short names.</li>
      <li>Recommended icon sizes:
        <ul>
          <li><strong>16x16</strong> - Standard display size.</li>
          <li><strong>32x32</strong> - Best for high-DPI displays.</li>
          <li><strong>64x64</strong> - Maximum useful size for scalability</li>
        </ul
      </li>
      <li>Recommended image file formats:
        <ul>
          <li><strong>SVG</strong> - Best choice (scalable, sharp at any size, small file size).</li>
          <li><strong>PNG</strong> - Good for raster images (use 32x32px or larger, then let CSS scale down).</li>
        </ul
      </li>
    </ul>
  </li><br>
  <li>Download the attached <code>userChrome.css</code> file (or create your own) and copy it into the <code>chrome</code> folder. Your folder structure should look like this:<br>
  <pre><code>firefox-profile/
└── chrome/
    ├── userChrome.css
    └── icons/
        ├── tools.svg
        ├── projects.png
        └── games.svg
</code></pre>
  </li>
  <li>Update bookmark labels and URLs in the CSS to match your folder and icon names.<br>
    <ul>
      <li>The <code>.bookmark-item</code> label should match the name of your bookmark folder.</li>
      <li>The <code>list-style: url</code> path should lead to the icon image file you would like to pair with the bookmark.</li>
      <li>The format should look like:</li>
    </ul>
    <pre><code>.bookmark-item[label=<strong>"Tools"</strong>] {  list-style: url("./icons/<strong>tools.svg</strong>") !important; }
.bookmark-item[label=<strong>"Projects"</strong>] {  list-style: url("./icons/<strong>project.png</strong>") !important; }
.bookmark-item[label=<strong>"Games"</strong>] {  list-style: url("./icons/<strong>games.svg</strong>") !important; }</code></pre>
</li>
  <li>Save your changes to <code>userChrome.css</code> and restart Firefox to apply the changes!</li>
</ol>
