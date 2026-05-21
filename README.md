<div align="center">
  <h1>📄 PDF Viewer for GitHub Pages</h1>

[![Codacy Badge](https://app.codacy.com/project/badge/Grade/3b39ac303ed846328479fd4273d04589)](https://app.codacy.com/gh/R0mb0/PDF_Viewer_for_GitHub_Pages/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)
[![pages-build-deployment](https://github.com/R0mb0/PDF_Viewer_for_GitHub_Pages/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/R0mb0/PDF_Viewer_for_GitHub_Pages/actions/workflows/pages/pages-build-deployment)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/R0mb0/PDF_Viewer_for_GitHub_Pages)
[![Open Source Love svg3](https://badges.frapsoft.com/os/v3/open-source.svg?v=103)](https://github.com/R0mb0/PDF_Viewer_for_GitHub_Pages)
[![MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/license/mit)
[![Donate](https://img.shields.io/badge/PayPal-Donate%20to%20Author-blue.svg)](http://paypal.me/R0mb0)
  
  <p>
    A lightweight, mobile-friendly static page to preview a PDF using the browser’s native viewer when available,
    with reliable fallback actions (open in a new tab / download) when inline PDF rendering isn’t supported.
  </p>
</div>

<div align="center">
  <a href="http://paypal.me/R0mb0">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://github.com/R0mb0/Support_the_dev_badge/blob/main/Badge/SVG/Support_the_dev_badge_Dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://github.com/R0mb0/Support_the_dev_badge/blob/main/Badge/SVG/Support_the_dev_badge_Light.svg">
      <img alt="Saved you time? Support the dev" src="https://github.com/R0mb0/Support_the_dev_badge/blob/main/Badge/SVG/Support_the_dev_badge_Default.svg">
    </picture>
  </a>
</div>

<div align="center">

## [👉 Click here to see the site! 👈](https://r0mb0.github.io/PDF_Viewer_for_GitHub_Pages/)

[![01.png](https://github.com/R0mb0/PDF_Viewer_for_GitHub_Pages/blob/main/Readme_imgs/01.png)](https://r0mb0.github.io/PDF_Viewer_for_GitHub_Pages/)

</div>

<hr>

<h2>🚀 Features</h2>
<ul>
  <li><strong>Native PDF Preview</strong>: Uses the browser’s built-in PDF renderer via <code>&lt;object&gt;</code> when supported.</li>
  <li><strong>Automatic Fallback</strong>: If inline preview is blocked (common on iOS/Safari), the page shows a fallback panel with <em>Open</em> and <em>Download</em> actions.</li>
  <li><strong>GitHub Pages Ready</strong>: Designed to work as a simple static site (no build step, no server required).</li>
  <li><strong>Clean UI</strong>: Minimal layout with an emphasis on readability and fast access to the PDF.</li>
  <li><strong>Light/Dark Auto Theme</strong>: Adapts to <code>prefers-color-scheme</code> for a consistent look.</li>
</ul>

<h2>🧠 How it works</h2>
<ol>
  <li><strong>Page loads</strong>: The UI is rendered instantly (static HTML/CSS).</li>
  <li><strong>PDF embed</strong>: The PDF is embedded using:
    <pre><code>&lt;object data="./Document.pdf" type="application/pdf"&gt;...&lt;/object&gt;</code></pre>
  </li>
  <li><strong>Preview or fallback</strong>:
    <ul>
      <li>If the browser supports inline PDF viewing, the document is displayed directly.</li>
      <li>If it doesn’t, the browser automatically shows the fallback HTML contained inside the <code>&lt;object&gt;</code>.</li>
    </ul>
  </li>
  <li><strong>User actions</strong>: The user can always open the PDF in a new tab or download it.</li>
</ol>

<h2>📁 Project structure</h2>
<ul>
  <li><code>index.html</code> — The main page (UI + PDF embed + fallback content).</li>
  <li><code>Document.pdf</code> — The PDF file to display (replace with your own).</li>
  <li><code>styles.css</code> — Optional external stylesheet (if you decide to move styles out of <code>index.html</code>).</li>
  <li><code>app.js</code> — Optional enhanced logic (health checks, loading overlay, timeout fallback) depending on the version you publish.</li>
</ul>

<h2>✅ Getting Started</h2>

<h3>1) Replace the PDF</h3>
<p>
  Put your PDF in the project root and name it <code>Document.pdf</code> (or update the references in <code>index.html</code> accordingly).
</p>

<h3>2) Run locally (recommended)</h3>
<p>
  Some browsers apply restrictions when opening files via <code>file:///</code>.
  To test reliably, use a small local web server.
</p>

<h4>Python</h4>
<ol>
  <li>Open a terminal in the project folder.</li>
  <li>Run:
    <ul>
      <li>macOS / Linux: <code>python3 -m http.server 8000</code></li>
      <li>Windows: <code>python -m http.server 8000</code></li>
    </ul>
  </li>
  <li>Open <code>http://localhost:8000</code></li>
</ol>

<h2>🌍 Deploy to GitHub Pages</h2>
<ol>
  <li>Push the repository to GitHub.</li>
  <li>Go to <strong>Settings</strong> → <strong>Pages</strong>.</li>
  <li>Select the branch (e.g. <code>main</code>) and the root folder (<code>/</code>).</li>
  <li>Wait for GitHub to publish the site, then open the provided URL.</li>
</ol>

<h2>⚠️ Compatibility notes</h2>
<ul>
  <li><strong>iOS / Safari</strong>: Inline PDF preview may be limited or disabled. The fallback actions (<em>Open</em>/<em>Download</em>) are the most reliable path.</li>
  <li><strong>Content-Type</strong>: Ensure your hosting serves the PDF with a correct MIME type (<code>application/pdf</code>). GitHub Pages typically handles this correctly.</li>
  <li><strong>Large PDFs</strong>: Very large documents may take longer to render; opening in a new tab is often smoother.</li>
</ul>

<a href="https://github.com/R0mb0/Not_made_by_AI">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/R0mb0/Not_made_by_AI/blob/main/Badge/SVG/NotMadeByAIDark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/R0mb0/Not_made_by_AI/blob/main/Badge/SVG/NotMadeByAILight.svg">
    <img alt="Not made by AI" src="https://github.com/R0mb0/Not_made_by_AI/blob/main/Badge/SVG/NotMadeByAIDefault.svg">
  </picture>
</a>
