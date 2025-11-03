<h1>Firefox Custom Bookmark Icons</h1>
<p>A simple guide and userChrome.css template for customizing bookmark favicons in Firefox.</p>
<ul>
  <li>Customize your folder icons.</li>
  <li>Replace missing or generic icons with custom images.</li>
  <li>Remove or edit the text formatting for your bookmarks.</li>
</ul>

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
  
  <li>Import your icon images into the <code>icons</code> folder.
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
