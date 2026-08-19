---
title: Admin
permalink: /admin/
---

<section class="section" style="margin-top:0;">
  <div class="section-header">
    <h1>Admin (Manual Content Management)</h1>
    <p>No database. All updates are made by editing Markdown/YAML files.</p>
  </div>

  <article class="card">
    <p>This website is designed for <strong>GitHub Pages + Markdown-based manual updates</strong>.</p>

    <h3>Content folders to edit</h3>
    <ul>
      <li><code>_people/</code> → members shown on People page</li>
      <li><code>_publications/</code> → publications list</li>
      <li><code>_news/</code> → news posts</li>
      <li><code>_gallery/</code> → gallery items</li>
    </ul>

    <h3>Admin workflow (manual approval)</h3>
    <ol>
      <li>Receive application by email.</li>
      <li>Review and decide approval.</li>
      <li>If approved, add one markdown file in <code>_people/</code>.</li>
      <li>Commit and push to GitHub.</li>
      <li>GitHub Pages updates the website automatically.</li>
    </ol>

    <h3>Markdown templates</h3>

<pre><code># People item (_people/your-name.md)
---
name: Jane Doe
role: Graduate Students
position: M.S. Student
order: 10
email: jane@example.com
interests: Robust perception, embodied AI
---

# Publication item (_publications/2026-paper.md)
---
title: "Paper Title"
authors: "Jane Doe, John Doe"
year: 2026
venue: "Conference Name"
link: "https://doi.org/..."
---

# News item (_news/2026-03-01-news.md)
---
title: "News Title"
date: 2026-03-01
summary: "One short summary sentence."
---

# Gallery item (_gallery/2026-photo.md)
---
title: "Lab Retreat 2026"
image: "/assets/images/gallery/lab-retreat-2026.jpg"
---</code></pre>
  </article>
</section>
