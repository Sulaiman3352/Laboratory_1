# Laboratory Work №1 — Personal Website

> **Assignment:** Create a Personal Website using HTML & CSS  
> **File:** `index.html`  
> **Author:** Sulayman Seid Ymam

---

## Project Structure
```
lab1/
├── index.html      ← Main HTML file (all code lives here)
└── README.md       ← This file
```

---

## Task Requirements & Code Explanation

---

### ✅ Task 1 — HTML

**Requirement:** Create an HTML page with proper document structure, a page title, a name header with a brief description, and an embedded profile image.
```html
<!-- Document structure -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Page title shown in browser tab -->
  <title>Sulayman Seid Ymam | Personal Website</title>
</head>
<body>

  <header>
    <!-- Profile image embedded via <img> with src attribute -->
    <img
      class="profile-img"
      src="./pic.jpg"
      alt="Profile photo of Sulayman Seid Ymam"
    />

    <!-- Name displayed using <h1> -->
    <h1>Sulayman Seid Ymam</h1>

    <!-- Brief description using <p> -->
    <p>Information Technology Student · DevOps Engineer · Tech Enthusiast</p>
  </header>

</body>
</html>
```

**Why:** The `<!DOCTYPE html>` declaration tells the browser this is an HTML5 document. `<html>`, `<head>`, and `<body>` form the required skeleton of every web page. `<title>` sets the browser tab label. `<h1>` is the top-level heading (used once, for the name), and `<p>` holds the short bio. The `<img>` tag uses the `src` attribute to point to the image source and `alt` for accessibility.

---

### ✅ Task 2 — About Me

**Requirement:** Create an "About Me" section using `<section>` or `<div>`, with a paragraph about interests, hobbies, and goals.
```html
<!-- About Me section identified by id for navigation -->
<section id="about">
  <h2>About Me</h2>
  <p>
    I'm a 3rd-year Information Technology student at Lobachevsky University,
    but my real passion lies in DevOps. I love working close to the metal —
    setting up Linux servers, writing automation scripts, containerising services,
    and making systems talk to each other reliably. I believe great infrastructure
    should be invisible: fast, stable, and self-healing. When I'm not tinkering
    with servers, I'm exploring new tools in the open-source ecosystem.
  </p>
</section>
```

**Why:** `<section>` is a semantic HTML5 element that groups related content. The `id="about"` attribute lets the navigation menu link directly to this section via `href="#about"`. The `<p>` tag holds the paragraph covering interests (*Linux servers, automation*), hobbies (*open-source tools*), and goals (*reliable, self-healing infrastructure*).

---

### ✅ Task 3 — Education and Skills

**Requirement:** Add "Education" and "Skills" sections using `<ul>` and `<li>` to list education history and key skills.
```html
<section id="education">
  <h2>Education &amp; Skills</h2>
  <div class="two-col">

    <!-- Education list -->
    <div>
      <h3>Education</h3>
      <ul class="styled-list">
        <li>B.Sc. Information Technology — Lobachevsky University (2023–2027)</li>
        <li>IT Specialist — Google (2021)</li>
        <li>Network Security — Microsoft (2024)</li>
      </ul>
    </div>

    <!-- Skills list -->
    <div>
      <h3>Key Skills</h3>
      <ul class="styled-list">
        <li><span class="icon">🐧</span> Linux</li>
        <li><span class="icon">🐚</span> Bash Scripting</li>
        <li><span class="icon">🐍</span> Python Scripting</li>
        <li><span class="icon">📦</span> Docker</li>
        <li><span class="icon">🖥️</span> Virtualization</li>
        <li><span class="icon">⚙️</span> Ansible</li>
      </ul>
    </div>

  </div>
</section>
```

**Why:** `<ul>` (unordered list) is the correct element for items that have no specific ranking order. Each `<li>` (list item) holds one entry. Two `<ul>` lists are placed side-by-side inside a flex `<div class="two-col">` for a clean two-column layout.

---

### ✅ Task 4 — Projects

**Requirement:** Create a "My Projects" section introducing a few projects using lists and descriptions.
```html
<section id="projects">
  <h2>My Projects</h2>
  <div class="projects-grid">

    <!-- Project 1 — Python Web Scraper -->
    <div class="project-card">
      <h3>🕷️ Python Web Scraper</h3>
      <p>A Python-based scraping tool that extracts structured data from target websites,
         handles pagination, rate-limiting, and exports results to JSON or CSV.</p>
      <ul class="feature-list">
        <li>Built with <code>requests</code> and <code>BeautifulSoup</code></li>
        <li>Automatic retry logic and request throttling</li>
        <li>Configurable via CLI arguments for different target sites</li>
        <li>Exports to JSON / CSV with timestamped output files</li>
      </ul>
      <span class="tag">Python</span>
      <span class="tag">BeautifulSoup</span>
      <span class="tag">Bash</span>
      <span class="tag">Linux</span>
    </div>

    <!-- Project 2 — Claude Storage Server -->
    <div class="project-card">
      <h3>🗄️ Claude Storage Server</h3>
      <p>Designed and deployed a self-hosted storage backend server to support
         Claude-related workflows, provisioned on Linux with containerised services
         managed via Docker.</p>
      <ul class="feature-list">
        <li>Provisioned on a Linux VM with custom networking rules</li>
        <li>Services containerised with Docker Compose</li>
        <li>Automated setup and re-deployment using Ansible playbooks</li>
        <li>Persistent volume management and backup scripting in Bash</li>
      </ul>
      <span class="tag">Docker</span>
      <span class="tag">Ansible</span>
      <span class="tag">Linux</span>
      <span class="tag">Bash</span>
      <span class="tag">Virtualization</span>
    </div>

    <!-- Project 3 — Multimedia Streaming Server -->
    <div class="project-card">
      <h3>📡 Multimedia Streaming Server</h3>
      <p>Built and configured a self-hosted multimedia streaming server on Linux,
         enabling on-demand video and audio access across the local network and
         remotely via a secure tunnel.</p>
      <ul class="feature-list">
        <li>Deployed Jellyfin inside a Docker container</li>
        <li>Configured reverse proxy and SSL with Nginx</li>
        <li>Automated library scanning and metadata fetching</li>
        <li>Remote access secured via WireGuard VPN tunnel</li>
      </ul>
      <span class="tag">Docker</span>
      <span class="tag">Nginx</span>
      <span class="tag">Linux</span>
      <span class="tag">WireGuard</span>
      <span class="tag">Ansible</span>
    </div>

  </div>
</section>
```

**Why:** Each project is wrapped in a `<div class="project-card">` block element. The project name uses `<h3>` (sub-heading level 3), `<p>` gives the description, `<ul>`+`<li>` lists the key features, and `<span class="tag">` displays the technology stack as small inline badges.

---

### ✅ Task 5 — CSS

**Requirement:** Include an external stylesheet via `<link>`, apply text and background colors with `color` and `background-color`, and choose a font using `font-family`.
```html
<!-- External stylesheet linked in <head> -->
<link rel="stylesheet" href="style.css" />

<!-- Google Fonts loaded as an external resource -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet" />
```
```css
/* font-family property — sets the typeface for the whole page */
body {
  font-family: 'Inter', sans-serif;

  /* background-color property — page background */
  background-color: #f4f6fb;

  /* color property — default text color */
  color: #2d2d2d;
}

/* Different background and text colors applied to the header */
header {
  background-color: #1a1a2e;
  color: #ffffff;
}

/* Navigation links use a distinct color */
nav ul li a {
  color: #e0e0e0;
}
```

**Why:** Separating styles into an external `style.css` file keeps HTML clean and allows one stylesheet to be reused across multiple pages. The `font-family` property controls typography. `background-color` and `color` are used on `body`, `header`, `nav`, `footer`, and individual components to create visual contrast and hierarchy.

---

### ✅ Task 6 — Layout

**Requirement:** Use block and inline elements to control layout, and apply styling using CSS selectors targeting specific elements.

#### Block elements used:
| Element | Role |
|---|---|
| `<header>` | Full-width page header block |
| `<nav>` | Full-width sticky navigation bar |
| `<main>` | Central content wrapper |
| `<section>` | Each content area (About, Education, Projects) |
| `<div class="project-card">` | Individual project block |

#### Inline elements used:
| Element | Role |
|---|---|
| `<span class="tag">` | Technology badge rendered inline within text flow |
| `<a>` | Navigation and footer links (inline) |

#### Selectors targeting specific elements:
```css
/* ID selector — styles only the About section's paragraph */
#about p {
  font-size: 1.05rem;
  color: #444;
}

/* Class + pseudo-class selector — hover effect on project cards only */
.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(127,90,240,0.12);
}

/* Element + pseudo-element selector — decorative underline on all h2 headings */
section h2::after {
  content: '';
  display: block;
  width: 48px;
  height: 3px;
  background-color: #7f5af0;
}
```

**Why:** Block elements stack vertically and take up full available width, making them ideal for page sections. Inline elements flow within text and are used for small decorative pieces like tags. CSS selectors (`#id`, `.class`, `element`, `:hover`, `::after`) allow precise, targeted styling without touching unrelated elements.

---

### ✅ Task 7 — Links and Navigation

**Requirement:** Add a navigation menu using `<ul>` and `<a>` elements, and create links to navigate between sections.
```html
<!-- Sticky navigation bar stays visible while scrolling -->
<nav>
  <ul>
    <!-- Each <li> holds one <a> anchor link -->
    <li><a href="#about">About</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
```
```css
/* Navigation bar container */
nav {
  position: sticky;  /* stays at top of viewport while scrolling */
  top: 0;
  z-index: 100;
  background-color: #1a1a2e;
}

/* Horizontal layout for nav items */
nav ul {
  list-style: none;
  display: flex;
  gap: 32px;
  justify-content: center;
}

/* Link color change on hover */
nav ul li a:hover {
  color: #7f5af0;
}
```

**Why:** `<ul>` is used as the container for navigation links — this is the standard, semantically correct HTML pattern for menus. Each `<a href="#sectionId">` uses an **anchor link** (the `#` symbol followed by an element's `id`) to scroll the user to the matching section on the same page. `position: sticky` keeps the nav bar visible at the top as the user scrolls, improving usability.

---

## Clean Code Principles Applied

| Principle | How it's applied |
|---|---|
| **Clear naming** | Classes named by purpose: `.project-card`, `.styled-list`, `.two-col` |
| **Comments** | Every major HTML block and CSS section has a descriptive `/* === */` comment |
| **Separation of concerns** | Structure in HTML, presentation in CSS (via `<link>` to external sheet) |
| **Semantic HTML** | `<nav>`, `<header>`, `<main>`, `<section>`, `<footer>` used over generic `<div>` where appropriate |
| **DRY (Don't Repeat Yourself)** | Shared styles (e.g. `.styled-list`, `section h2`) defined once and reused |
| **Accessibility** | `alt` attribute on `<img>`, `lang="en"` on `<html>`, logical heading hierarchy (`h1` → `h2` → `h3`) |
