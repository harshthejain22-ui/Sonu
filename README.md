/* Color Palette & Variables */
:root {
  --bg-main: #0a0e17;       /* Deep Navy Black */
  --bg-card: #121824;       /* Charcoal Navy */
  --bg-card-hover: #1a2234;
  --accent-navy: #1e293b;
  --text-white: #ffffff;
  --text-primary: #e2e8f0;  /* Crisp Off-White */
  --text-muted: #94a3b8;    /* Charcoal Light Gray */
  --accent-silver: #cbd5e1;
  --border-color: #1e293b;
  --font-sans: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-mono: SFMono-Regular, Menlo, Monaco, Consolas, monospace;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-sans);
  background-color: var(--bg-main);
  color: var(--text-primary);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.font-mono {
  font-family: var(--font-mono);
}

/* Typography & Buttons */
h1, h2, h3, h4 {
  color: var(--text-white);
  font-weight: 600;
  letter-spacing: -0.02em;
}

a {
  color: inherit;
  text-decoration: none;
}

.btn {
  display: inline-block;
  padding: 0.85rem 1.75rem;
  font-size: 0.9rem;
  font-weight: 600;
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.25s ease;
  border: 1px solid transparent;
}

.btn-primary {
  background-color: var(--text-white);
  color: var(--bg-main);
}

.btn-primary:hover {
  background-color: var(--accent-silver);
}

.btn-secondary {
  background-color: transparent;
  color: var(--text-white);
  border-color: var(--border-color);
}

.btn-secondary:hover {
  background-color: var(--accent-navy);
}

.btn-outline {
  border-color: var(--text-white);
  color: var(--text-white);
}

.btn-outline:hover {
  background-color: var(--text-white);
  color: var(--bg-main);
}

.btn-full {
  width: 100%;
}

/* Navigation */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: rgba(10, 14, 23, 0.9);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--border-color);
  z-index: 100;
  padding: 1.25rem 0;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.brand {
  font-size: 1.25rem;
  font-weight: 700;
  letter-spacing: 0.15em;
  color: var(--text-white);
}

.brand span {
  font-weight: 300;
  color: var(--text-muted);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.nav-links a {
  font-size: 0.88rem;
  color: var(--text-muted);
  transition: color 0.2s;
}

.nav-links a:hover {
  color: var(--text-white);
}

.mobile-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  flex-direction: column;
  gap: 5px;
}

.mobile-toggle span {
  width: 25px;
  height: 2px;
  background-color: var(--text-white);
}

/* Hero Section */
.hero {
  padding: 11rem 0 6rem 0;
  border-bottom: 1px solid var(--border-color);
}

.hero-container {
  max-width: 850px;
  text-align: center;
}

.badge {
  display: inline-block;
  font-size: 0.75rem;
  font-family: var(--font-mono);
  text-transform: uppercase;
  letter-spacing: 0.1em;
  padding: 0.4rem 0.9rem;
  border: 1px solid var(--border-color);
  border-radius: 50px;
  color: var(--text-muted);
  margin-bottom: 1.5rem;
}

.hero-title {
  font-size: 3.25rem;
  line-height: 1.15;
  margin-bottom: 1.5rem;
}

.hero-subtitle {
  font-size: 1.15rem;
  color: var(--text-muted);
  margin-bottom: 2.5rem;
  font-weight: 400;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  justify-content: center;
}

/* Metrics Bar */
.metrics-bar {
  border-bottom: 1px solid var(--border-color);
  background-color: var(--bg-card);
  padding: 2.5rem 0;
}

.metrics-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  text-align: center;
  gap: 2rem;
}

.metric-number {
  display: block;
  font-size: 2.25rem;
  font-weight: 700;
  color: var(--text-white);
}

.metric-label {
  font-size: 0.8rem;
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

/* Section Common Layouts */
.section {
  padding: 7rem 0;
  border-bottom: 1px solid var(--border-color);
}

.section-header {
  margin-bottom: 4rem;
}

.section-tag {
  font-size: 0.8rem;
  color: var(--text-muted);
  letter-spacing: 0.1em;
  display: block;
  margin-bottom: 0.5rem;
}

.section-header h2 {
  font-size: 2.25rem;
  margin-bottom: 0.75rem;
}

.section-lead {
  color: var(--text-muted);
  font-size: 1.1rem;
}

/* Grids & Cards */
.grid {
  display: grid;
  gap: 2rem;
}

.grid-3 {
  grid-template-columns: repeat(3, 1fr);
}

.card {
  background-color: var(--bg-card);
  border: 1px solid var(--border-color);
  padding: 2.5rem;
  border-radius: 6px;
  transition: transform 0.25s ease, border-color 0.25s ease;
}

.card:hover {
  border-color: #334155;
  transform: translateY(-4px);
}

.burnout-card .card-num {
  font-size: 0.9rem;
  color: var(--text-muted);
  margin-bottom: 1.5rem;
}

.burnout-card h3 {
  font-size: 1.25rem;
  margin-bottom: 1rem;
}

.burnout-card p {
  color: var(--text-muted);
  font-size: 0.95rem;
}

/* Resource Section Filters & Cards */
.filter-controls {
  display: flex;
  gap: 0.75rem;
  margin-bottom: 3rem;
  flex-wrap: wrap;
}

.filter-btn {
  background-color: transparent;
  border: 1px solid var(--border-color);
  color: var(--text-muted);
  padding: 0.5rem 1.25rem;
  font-size: 0.85rem;
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.2s;
}

.filter-btn:hover, .filter-btn.active {
  color: var(--text-white);
  border-color: var(--text-white);
  background-color: var(--accent-navy);
}

.article-card .article-category {
  font-size: 0.75rem;
  font-family: var(--font-mono);
  color: var(--text-muted);
  text-transform: uppercase;
  display: block;
  margin-bottom: 1rem;
}

.article-card h3 {
  font-size: 1.15rem;
  margin-bottom: 1rem;
  line-height: 1.4;
}

.article-card p {
  color: var(--text-muted);
  font-size: 0.9rem;
  margin-bottom: 1.5rem;
}

.read-more {
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--text-white);
}

/* Modal Window */
.modal {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(10, 14, 23, 0.85);
  backdrop-filter: blur(8px);
  z-index: 1000;
  align-items: center;
  justify-content: center;
}

.modal.active {
  display: flex;
}

.modal-content {
  background-color: var(--bg-card);
  border: 1px solid var(--border-color);
  padding: 3rem;
  border-radius: 8px;
  max-width: 500px;
  width: 90%;
  position: relative;
}

.modal-close {
  position: absolute;
  top: 1.5rem;
  right: 1.5rem;
  background: none;
  border: none;
  color: var(--text-muted);
  font-size: 1.75rem;
  cursor: pointer;
}

.form-group {
  margin-top: 1.5rem;
}

.form-group label {
  display: block;
  font-size: 0.85rem;
  color: var(--text-muted);
  margin-bottom: 0.5rem;
}

.form-group input, .form-group select {
  width: 100%;
  padding: 0.8rem;
  background-color: var(--bg-main);
  border: 1px solid var(--border-color);
  color: var(--text-white);
  border-radius: 4px;
}

.form-group input:focus, .form-group select:focus {
  outline: none;
  border-color: var(--accent-silver);
}

/* Footer & Bold Medical Disclaimer */
.footer {
  padding: 5rem 0 3rem 0;
  background-color: var(--bg-main);
}

.footer-top {
  display: flex;
  justify-content: space-between;
  margin-bottom: 3.5rem;
}

.footer-brand p {
  color: var(--text-muted);
  font-size: 0.9rem;
  margin-top: 0.5rem;
}

.footer-links h4 {
  font-size: 0.9rem;
  margin-bottom: 1rem;
}

.footer-links ul {
  list-style: none;
}

hvhjvv
