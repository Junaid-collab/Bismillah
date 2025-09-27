# Junaid-statistics
Statistical R codes
github.com/junaid-collab
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Repo Site</title>
  <meta name="description" content="A simple static site generated from a GitHub repo" />
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#9aa4b2; --accent:#7dd3fc;
      --glass: rgba(255,255,255,0.03);
    }
    *{box-sizing:border-box}
    body{
      margin:0; font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,#071021 0%, #071827 60%); color:#e6eef6;
      padding:24px;
      -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
    }
    .wrap{max-width:980px;margin:0 auto;}
    header{display:flex;gap:16px;align-items:center;margin-bottom:18px}
    .logo{
      width:64px;height:64px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#4f46e5);
      display:flex;align-items:center;justify-content:center;font-weight:700;color:#06202a;
      box-shadow:0 6px 20px rgba(2,6,23,0.6);
    }
    h1{margin:0;font-size:20px}
    p.lead{margin:4px 0 0;color:var(--muted)}
    .grid{display:grid;grid-template-columns:1fr 360px;gap:18px;margin-top:18px}
    @media (max-width:880px){ .grid{grid-template-columns:1fr} .right{order:2} }
    .card{background:var(--card);padding:16px;border-radius:12px;box-shadow:0 6px 20px rgba(2,6,23,0.6)}
    .muted{color:var(--muted);font-size:13px}
    .file-list{list-style:none;padding:0;margin:0}
    .file-list li{padding:8px 10px;border-radius:8px;display:flex;justify-content:space-between;gap:10px;align-items:center}
    .file-list li:hover{background:var(--glass)}
    .tag{background:rgba(255,255,255,0.03);padding:4px 8px;border-radius:999px;font-size:12px;color:var(--muted)}
    a.inline{color:var(--accent);text-decoration:none}
    footer{margin-top:18px;color:var(--muted);font-size:13px}
    /* README styling */
    .readme img{max-width:100%;}
    pre{background:#041022;padding:12px;border-radius:8px;overflow:auto}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">GH</div>
      <div>
        <h1 id="repo-title">Repository</h1>
        <p class="lead" id="repo-desc">Automatically generated site from repo files.</p>
      </div>
      <div style="margin-left:auto; text-align:right">
        <div class="muted">Static site • GitHub Pages</div>
        <div style="margin-top:6px"><a id="repo-link" class="inline" href="#" target="_blank">Open on GitHub →</a></div>
      </div>
    </header>

    <div class="grid">
      <main>
        <div class="card">
          <h3 style="margin-top:0">README</h3>
          <div id="readme" class="readme muted">Loading README...</div>
        </div>

        <div class="card" style="margin-top:12px">
          <h3 style="margin-top:0">Files</h3>
          <ul id="files" class="file-list">
            <li class="muted">Loading files…</li>
          </ul>
        </div>
      </main>

      <aside class="right">
        <div class="card">
          <h4 style="margin-top:0">Repo info</h4>
          <div class="muted" id="repo-meta">Loading meta…</div>
          <hr style="margin:12px 0;border:none;border-top:1px solid rgba(255,255,255,0.03)">
          <div class="muted">Quick actions</div>
          <div style="margin-top:10px;display:flex;gap:8px">
            <a id="open-issues" class="tag inline" target="_blank">Issues</a>
            <a id="open-pulls" class="tag inline" target="_blank">Pulls</a>
            <a id="open-actions" class="tag inline" target="_blank">Actions</a>
          </div>
        </div>

        <div class="card" style="margin-top:12px">
          <div class="muted">How to customize</div>
          <ol style="margin:10px 0 0 18px;color:var(--muted);font-size:14px">
            <li>Change the HTML/CSS in <code>index.html</code>.</li>
            <li>Add pages like <code>about.html</code> or <code>docs/</code>.</li>
            <li>Enable GitHub Pages in your repo settings.</li>
          </ol>
        </div>
      </aside>
    </div>

    <footer>
      Need advanced features? Add client-side search, or use a static site generator (Jekyll, Hugo, or VitePress).
    </footer>
  </div>

  <!-- External helpers: marked to render Markdown, DOMPurify to sanitize -->
  <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/dompurify/dist/purify.min.js"></script>

  <script>
    // === CONFIGURE HERE ===
    const OWNER = "OWNER"; // e.g. "your-username" or organization
    const REPO  = "REPO";
