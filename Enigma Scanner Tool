<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Group 8 IT 304 – Enigma Scanner</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    /* ==========================
       GLOBAL STYLES (EASY TO EDIT)
       ========================== */
    :root {
      /* Main colors – customize these */
      --bg-color: #050816;
      --bg-alt: #0b1020;
      --accent: #4f46e5;
      --accent-soft: rgba(79, 70, 229, 0.12);
      --accent-strong: rgba(79, 70, 229, 0.25);
      --text-main: #f9fafb;
      --text-muted: #9ca3af;
      --border-subtle: #1f2933;
      --card-bg: #0b1020;
      --card-bg-alt: #050816;
      --danger: #f97373;
      --success: #4ade80;
      --warning: #fb923c;
      --shadow-soft: 0 22px 60px rgba(15, 23, 42, 0.6);
      --radius-xl: 20px;
      --radius-2xl: 26px;
      --radius-pill: 999px;
      --transition-fast: 0.18s ease-out;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #111827 0, #020617 45%, #000 100%);
      color: var(--text-main);
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    img {
      max-width: 100%;
      display: block;
      border-radius: 18px;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: 100%;
      max-width: 1120px;
      margin: 0 auto;
      padding: 0 1.25rem;
    }

    /* ==========================
       HEADER / NAV
       ========================== */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(14px);
      background: linear-gradient(to bottom, rgba(5, 6, 14, 0.95), rgba(5, 6, 14, 0.6));
      border-bottom: 1px solid rgba(148, 163, 184, 0.08);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.9rem 0.25rem;
      gap: 1.5rem;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .brand-logo {
      width: 40px;
      height: 40px;
      border-radius: 30%;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at 30% 0%, #6366f1, #22d3ee 45%, #0f172a 100%);
      box-shadow: 0 12px 30px rgba(37, 99, 235, 0.45);
      font-weight: 700;
      letter-spacing: 0.04em;
      font-size: 0.8rem;
    }

    .brand-text {
      display: flex;
      flex-direction: column;
      gap: 0.1rem;
    }

    .brand-text .title {
      font-size: 0.9rem;
      font-weight: 600;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: #e5e7eb;
    }

    .brand-text .subtitle {
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1rem;
      font-size: 0.9rem;
    }

    nav li a {
      padding: 0.4rem 0.75rem;
      border-radius: 999px;
      color: var(--text-muted);
      border: 1px solid transparent;
      transition: background var(--transition-fast), color var(--transition-fast), border-color var(--transition-fast), transform var(--transition-fast);
      font-size: 0.85rem;
    }

    nav li a:hover {
      background: rgba(15, 23, 42, 0.9);
      border-color: rgba(148, 163, 184, 0.35);
      color: #e5e7eb;
      transform: translateY(-1px);
    }

    .nav-cta {
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .badge-pill {
      font-size: 0.75rem;
      padding: 0.25rem 0.6rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(148, 163, 184, 0.3);
      color: var(--text-muted);
      background: rgba(15, 23, 42, 0.75);
    }

    .btn-outline {
      font-size: 0.8rem;
      padding: 0.4rem 0.95rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(79, 70, 229, 0.65);
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.3), transparent 60%);
      color: #e5e7eb;
      display: inline-flex;
      align-items: center;
      gap: 0.35rem;
      cursor: pointer;
      transition: background var(--transition-fast), transform var(--transition-fast), box-shadow var(--transition-fast), border-color var(--transition-fast);
      box-shadow: 0 10px 25px rgba(79, 70, 229, 0.35);
    }

    .btn-outline span.icon {
      font-size: 1rem;
    }

    .btn-outline:hover {
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.45), rgba(15, 23, 42, 0.95) 70%);
      transform: translateY(-1px) translateX(0);
      box-shadow: 0 18px 40px rgba(79, 70, 229, 0.55);
      border-color: rgba(129, 140, 248, 0.9);
    }

    /* ==========================
       HERO SECTION
       ========================== */
    .hero {
      padding: 3.4rem 0 2.6rem;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.25fr) minmax(0, 1.1fr);
      gap: 2.4rem;
      align-items: center;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.2rem 0.4rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(148, 163, 184, 0.35);
      background: rgba(15, 23, 42, 0.8);
      margin-bottom: 0.9rem;
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    .eyebrow-pill {
      padding: 0.1rem 0.5rem;
      border-radius: var(--radius-pill);
      background: rgba(55, 65, 81, 0.9);
      color: #e5e7eb;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 0.06em;
    }

    .eyebrow-dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: radial-gradient(circle, #22c55e 0, #16a34a 80%);
      box-shadow: 0 0 0 6px rgba(22, 163, 74, 0.25);
    }

    .hero-title {
      font-size: clamp(2.15rem, 3.1vw + 1rem, 2.9rem);
      font-weight: 700;
      letter-spacing: 0.02em;
      margin-bottom: 0.7rem;
    }

    .hero-title span.highlight {
      background: linear-gradient(90deg, #38bdf8, #a855f7, #f97316);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: 0 0 40px rgba(56, 189, 248, 0.3);
    }

    .hero-subtitle {
      font-size: 0.98rem;
      color: var(--text-muted);
      max-width: 34rem;
      margin-bottom: 1.4rem;
    }

    .hero-meta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      margin-bottom: 1.6rem;
      font-size: 0.77rem;
    }

    .meta-pill {
      padding: 0.35rem 0.7rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(148, 163, 184, 0.3);
      color: var(--text-muted);
      background: rgba(15, 23, 42, 0.85);
      display: inline-flex;
      align-items: center;
      gap: 0.35rem;
      white-space: nowrap;
    }

    .meta-pill strong {
      color: #e5e7eb;
      font-weight: 500;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      margin-bottom: 1.6rem;
    }

    .btn-primary {
      padding: 0.65rem 1.25rem;
      border-radius: var(--radius-pill);
      border: none;
      cursor: pointer;
      background: linear-gradient(135deg, #6366f1, #22d3ee);
      color: white;
      font-weight: 500;
      font-size: 0.9rem;
      display: inline-flex;
      align-items: center;
      gap: 0.45rem;
      box-shadow: 0 18px 40px rgba(15, 23, 42, 0.65);
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), filter var(--transition-fast);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      filter: brightness(1.07);
      box-shadow: 0 26px 60px rgba(15, 23, 42, 0.85);
    }

    .btn-ghost {
      padding: 0.6rem 1.1rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(148, 163, 184, 0.45);
      background: transparent;
      color: var(--text-muted);
      font-size: 0.85rem;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      cursor: pointer;
      transition: background var(--transition-fast), border-color var(--transition-fast), color var(--transition-fast), transform var(--transition-fast);
    }

    .btn-ghost:hover {
      background: rgba(15, 23, 42, 0.9);
      border-color: rgba(148, 163, 184, 0.9);
      color: #e5e7eb;
      transform: translateY(-1px);
    }

    .hero-footnote {
      font-size: 0.76rem;
      color: var(--text-muted);
    }

    .hero-footnote span {
      color: #e5e7eb;
      font-weight: 500;
    }

    /* HERO VISUAL PANEL */
    .hero-visual-card {
      position: relative;
      border-radius: var(--radius-2xl);
      padding: 1.2rem;
      background: radial-gradient(circle at top left, #111827, #020617 55%, #000 100%);
      border: 1px solid rgba(148, 163, 184, 0.16);
      box-shadow: var(--shadow-soft);
      overflow: hidden;
      min-height: 310px;
    }

    .hero-visual-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.9rem;
    }

    .hero-visual-title {
      font-size: 0.85rem;
      color: var(--text-muted);
    }

    .hero-visual-title span {
      display: block;
      font-size: 1.05rem;
      color: #e5e7eb;
      font-weight: 500;
    }

    .hero-visual-dots {
      display: flex;
      gap: 0.4rem;
    }

    .hero-visual-dot {
      width: 9px;
      height: 9px;
      border-radius: 999px;
      background: #111827;
      border: 1px solid rgba(148, 163, 184, 0.5);
    }

    .hero-visual-dot.red {
      background: #f97373;
      border-color: rgba(248, 113, 113, 0.8);
    }

    .hero-visual-dot.amber {
      background: #fb923c;
      border-color: rgba(251, 146, 60, 0.8);
    }

    .hero-visual-dot.green {
      background: #4ade80;
      border-color: rgba(74, 222, 128, 0.8);
    }

    .hero-visual-body {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.95fr);
      gap: 1.1rem;
      align-items: stretch;
    }

    .scan-preview {
      background: radial-gradient(circle at top, #1f2937, #020617 65%);
      border-radius: 18px;
      padding: 0.7rem;
      border: 1px solid rgba(148, 163, 184, 0.25);
      position: relative;
    }

    .scan-preview-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.6rem;
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    .scan-preview-badges {
      display: flex;
      gap: 0.35rem;
    }

    .scan-badge {
      padding: 0.15rem 0.45rem;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.5);
      font-size: 0.7rem;
      display: inline-flex;
      align-items: center;
      gap: 0.25rem;
    }

    .scan-badge span.dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: var(--success);
      box-shadow: 0 0 0 3px rgba(74, 222, 128, 0.3);
    }

    .scan-image-wrapper {
      position: relative;
      overflow: hidden;
      border-radius: 14px;
      border: 1px solid rgba(148, 163, 184, 0.3);
    }

    .scan-tag {
      position: absolute;
      top: 0.6rem;
      left: 0.6rem;
      padding: 0.25rem 0.55rem;
      border-radius: var(--radius-pill);
      font-size: 0.7rem;
      font-weight: 500;
      background: rgba(15, 23, 42, 0.8);
      border: 1px solid rgba(148, 163, 184, 0.7);
    }

    .scan-tag.ai {
      right: 0.6rem;
      left: auto;
      background: rgba(124, 58, 237, 0.9);
      border-color: rgba(192, 132, 252, 0.9);
    }

    .scan-score-bar {
      position: absolute;
      bottom: 0.6rem;
      left: 0.7rem;
      right: 0.7rem;
      padding: 0.35rem 0.5rem;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.6);
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.7rem;
      gap: 0.4rem;
    }

    .score-labels {
      display: flex;
      gap: 0.4rem;
      align-items: center;
    }

    .score-labels span {
      font-weight: 500;
    }

    .score-bar-track {
      flex: 1;
      height: 6px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.95);
      overflow: hidden;
      display: flex;
    }

    .score-real {
      flex: 0 0 55%;
      background: linear-gradient(90deg, #4ade80, #22c55e);
    }

    .score-ai {
      flex: 0 0 45%;
      background: linear-gradient(90deg, #f97373, #ef4444);
    }

    .score-caption {
      font-size: 0.68rem;
      color: var(--text-muted);
    }

    .hero-visual-side {
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
      font-size: 0.8rem;
    }

    .hero-visual-pill {
      padding: 0.45rem 0.6rem;
      border-radius: 14px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.3);
      color: var(--text-muted);
    }

    .hero-visual-pill strong {
      display: block;
      font-size: 0.85rem;
      color: #e5e7eb;
      margin-bottom: 0.15rem;
    }

    .hero-visual-stats {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.55rem;
    }

    .hero-stat {
      padding: 0.45rem 0.55rem;
      border-radius: 14px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.18), rgba(15, 23, 42, 0.95) 55%);
    }

    .hero-stat-label {
      font-size: 0.72rem;
      color: var(--text-muted);
    }

    .hero-stat-value {
      font-size: 0.95rem;
      font-weight: 600;
    }

    .hero-visual-footer {
      margin-top: auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    .hero-visual-footer span.badge {
      padding: 0.2rem 0.55rem;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.4);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }

    /* Light floating glow shapes */
    .glow-blob {
      position: absolute;
      border-radius: 999px;
      filter: blur(40px);
      opacity: 0.7;
      pointer-events: none;
    }

    .glow-blob.one {
      width: 130px;
      height: 130px;
      background: rgba(56, 189, 248, 0.3);
      top: -40px;
      right: -30px;
    }

    .glow-blob.two {
      width: 120px;
      height: 120px;
      background: rgba(168, 85, 247, 0.32);
      bottom: -40px;
      left: -30px;
    }

    /* ==========================
       SECTION WRAPPER
       ========================== */
    section {
      padding: 1.6rem 0;
    }

    section h2 {
      font-size: 1.4rem;
      margin-bottom: 0.25rem;
    }

    section p.section-intro {
      font-size: 0.9rem;
      color: var(--text-muted);
      max-width: 40rem;
    }

    /* ==========================
       FEATURE GRID
       ========================== */
    .feature-grid {
      margin-top: 1.2rem;
      display: grid;
      gap: 1rem;
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }

    .feature-card {
      border-radius: var(--radius-xl);
      padding: 0.9rem;
      border: 1px solid rgba(148, 163, 184, 0.25);
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.16), rgba(15, 23, 42, 0.96) 55%);
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), border-color var(--transition-fast), background var(--transition-fast);
      box-shadow: 0 14px 40px rgba(15, 23, 42, 0.6);
    }

    .feature-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 22px 60px rgba(15, 23, 42, 0.9);
      border-color: rgba(129, 140, 248, 0.85);
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.26), rgba(15, 23, 42, 1) 60%);
    }

    .feature-tag {
      font-size: 0.75rem;
      color: var(--text-muted);
      margin-bottom: 0.25rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .feature-title {
      font-size: 0.95rem;
      font-weight: 600;
      margin-bottom: 0.35rem;
    }

    .feature-text {
      font-size: 0.82rem;
      color: var(--text-muted);
      margin-bottom: 0.5rem;
    }

    .feature-meta {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.75rem;
      color: var(--text-muted);
      margin-top: 0.25rem;
    }

    .risk-chip {
      display: inline-flex;
      align-items: center;
      gap: 0.25rem;
      padding: 0.1rem 0.55rem;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.45);
      font-size: 0.72rem;
    }

    .risk-dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
    }

    .risk-high {
      background: var(--danger);
      box-shadow: 0 0 0 4px rgba(248, 113, 113, 0.4);
    }

    .risk-medium {
      background: var(--warning);
      box-shadow: 0 0 0 4px rgba(251, 146, 60, 0.4);
    }

    .risk-low {
      background: var(--success);
      box-shadow: 0 0 0 4px rgba(74, 222, 128, 0.4);
    }

    /* ==========================
       HOW IT WORKS (TIMELINE)
       ========================== */
    .timeline {
      margin-top: 1.1rem;
      display: grid;
      gap: 0.7rem;
    }

    .timeline-step {
      display: grid;
      grid-template-columns: 60px minmax(0, 1fr);
      gap: 0.8rem;
      align-items: start;
    }

    .timeline-number {
      width: 46px;
      height: 46px;
      border-radius: 999px;
      border: 1px solid rgba(129, 140, 248, 0.7);
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at top, rgba(129, 140, 248, 0.45), rgba(15, 23, 42, 0.95));
      font-size: 0.9rem;
      font-weight: 600;
    }

    .timeline-content {
      padding: 0.7rem 0.85rem;
      border-radius: 16px;
      background: rgba(15, 23, 42, 0.95);
      border: 1px solid rgba(148, 163, 184, 0.3);
      font-size: 0.8rem;
    }

    .timeline-content h3 {
      font-size: 0.9rem;
      margin-bottom: 0.25rem;
    }

    .timeline-content p {
      color: var(--text-muted);
    }

    /* ==========================
       IMAGE STRIP (REAL VS AI)
       ========================== */
    .image-strip {
      margin-top: 1.6rem;
      border-radius: var(--radius-2xl);
      padding: 1rem;
      background: radial-gradient(circle at top, #111827, #020617 50%, #000 100%);
      border: 1px solid rgba(148, 163, 184, 0.25);
      display: grid;
      grid-template-columns: minmax(0, 1fr) minmax(0, 1fr);
      gap: 1rem;
      align-items: stretch;
      box-shadow: var(--shadow-soft);
    }

    .image-strip-text {
      font-size: 0.88rem;
      color: var(--text-muted);
    }

    .image-strip-text h3 {
      font-size: 1.05rem;
      margin-bottom: 0.3rem;
    }

    .image-strip-text ul {
      margin-top: 0.4rem;
      padding-left: 1rem;
      font-size: 0.84rem;
    }

    .image-strip-text li {
      margin-bottom: 0.2rem;
    }

    .image-strip-gallery {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.5rem;
    }

    .image-card {
      position: relative;
      border-radius: 16px;
      overflow: hidden;
      border: 1px solid rgba(148, 163, 184, 0.25);
      background: linear-gradient(145deg, rgba(15, 23, 42, 0.9), #020617);
    }

    .image-card-label {
      position: absolute;
      top: 0.45rem;
      left: 0.45rem;
      padding: 0.2rem 0.55rem;
      border-radius: 999px;
      font-size: 0.7rem;
      font-weight: 500;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.6);
    }

    .image-card-label.ai {
      background: rgba(124, 58, 237, 0.9);
      border-color: rgba(192, 132, 252, 0.9);
    }

    .image-card-footer {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      padding: 0.35rem 0.5rem;
      font-size: 0.7rem;
      background: linear-gradient(to top, rgba(15, 23, 42, 0.95), transparent);
      color: var(--text-muted);
    }

    .image-card-footer strong {
      display: block;
      font-size: 0.78rem;
      color: #e5e7eb;
    }

    /* Placeholder image style */
    .placeholder-img {
      width: 100%;
      aspect-ratio: 4 / 3;
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.65), rgba(15, 23, 42, 0.98));
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.78rem;
      color: #d1d5db;
      text-align: center;
      padding: 0.8rem;
    }

    /* ==========================
       FAQ
       ========================== */
    .faq-grid {
      margin-top: 1.1rem;
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.9rem;
    }

    .faq-item {
      border-radius: 16px;
      padding: 0.7rem 0.85rem;
      border: 1px solid rgba(148, 163, 184, 0.25);
      background: rgba(15, 23, 42, 0.96);
      font-size: 0.8rem;
    }

    .faq-item h3 {
      font-size: 0.9rem;
      margin-bottom: 0.25rem;
    }

    .faq-item p {
      color: var(--text-muted);
    }

    /* ==========================
       FOOTER / AUTHORS
       ========================== */
    footer {
      margin-top: 2rem;
      padding: 1.4rem 0 2.2rem;
      border-top: 1px solid rgba(148, 163, 184, 0.2);
      background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
    }

    .footer-inner {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      align-items: center;
      justify-content: space-between;
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    .author-section {
      display: flex;
      flex-direction: column;
      gap: 0.25rem;
    }

    .author-section strong {
      color: #e5e7eb;
    }

    .author-names {
      display: inline-flex;
      flex-wrap: wrap;
      gap: 0.4rem;
    }

    .author-pill {
      padding: 0.2rem 0.6rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.5);
      background: rgba(15, 23, 42, 0.96);
    }

    /* ==========================
       RESPONSIVE
       ========================== */
    @media (max-width: 900px) {
      .hero-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-visual-card {
        order: -1;
      }

      .feature-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .image-strip {
        grid-template-columns: minmax(0, 1fr);
      }

      .image-strip-gallery {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .faq-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .nav {
        flex-wrap: wrap;
      }

      nav ul {
        display: none; /* hide full nav on mobile for simplicity */
      }
    }

    @media (max-width: 640px) {
      .feature-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .image-strip-gallery {
        grid-template-columns: minmax(0, 1fr);
      }
    }
  </style>
</head>
<body>
  <!-- ==========================
       HEADER / NAV
       ========================== -->
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="brand-logo">G8</div>
        <div class="brand-text">
          <span class="title">Group 8 IT 304</span>
          <span class="subtitle">Enigma Scanner • Real vs AI Image Intelligence</span>
        </div>
      </div>
      <nav aria-label="Primary navigation">
        <ul>
          <li><a href="#overview">Overview</a></li>
          <li><a href="#features">Features</a></li>
          <li><a href="#how-it-works">How It Works</a></li>
          <li><a href="#faq">FAQ</a></li>
        </ul>
      </nav>
      <div class="nav-cta">
        <div class="badge-pill">Prototype concept • AI detection demo</div>
        <button class="btn-outline" type="button">
          <span class="icon">⚡</span>
          Try a Sample Scan
        </button>
      </div>
    </div>
  </header>

  <!-- ==========================
       HERO
       ========================== -->
  <main>
    <section class="hero" id="overview">
      <div class="container hero-grid">
        <!-- HERO TEXT -->
        <div>
          <div class="eyebrow">
            <span class="eyebrow-dot"></span>
            <span class="eyebrow-pill">Enigma Scanner</span>
            <span>Real–vs–AI Image Intelligence</span>
          </div>

          <h1 class="hero-title">
            Detect <span class="highlight">AI-generated images</span>
            before they erode trust.
          </h1>

          <p class="hero-subtitle">
            Enigma Scanner is an AI-assisted inspection tool concept designed to help users quickly evaluate
            whether an image is likely human-made or AI-generated. It combines pixel-level artifacts,
            metadata inspection, and behavioral patterns to flag suspicious content and protect digital integrity.
          </p>

          <div class="hero-meta-row">
            <div class="meta-pill">
              <span>🎯</span> <strong>Use cases:</strong> academic work, journalism, security, content review
            </div>
            <div class="meta-pill">
              <span>🧠</span> <strong>Signals:</strong> compression noise, eye asymmetry, texture anomalies
            </div>
            <div class="meta-pill">
              <span>🛡️</span> <strong>Goal:</strong> support informed decisions, not replace human judgment
            </div>
          </div>

          <div class="hero-actions">
            <button class="btn-primary" type="button">
              🔍 Run Example Analysis
            </button>
            <button class="btn-ghost" type="button">
              📁 View Detection Criteria
            </button>
          </div>

          <p class="hero-footnote">
            <span>Note:</span> This page presents a conceptual design for a tool idea — ideal for class demos,
            design discussions, and project presentations.
          </p>
        </div>

        <!-- HERO VISUAL PANEL -->
        <div class="hero-visual-card" aria-label="Enigma Scanner analysis preview">
          <div class="hero-visual-header">
            <div class="hero-visual-title">
              Live Scan
              <span>Image Authenticity Dashboard</span>
            </div>
            <div class="hero-visual-dots">
              <div class="hero-visual-dot red"></div>
              <div class="hero-visual-dot amber"></div>
              <div class="hero-visual-dot green"></div>
            </div>
          </div>

          <div class="hero-visual-body">
            <!-- Scan preview box -->
            <div class="scan-preview">
              <div class="scan-preview-bar">
                <span>Sample Input: portrait.png</span>
                <div class="scan-preview-badges">
                  <div class="scan-badge">
                    <span class="dot"></span>
                    <span>Scan ready</span>
                  </div>
                  <div class="scan-badge">
                    ⏱ <span>~2.1s analysis</span>
                  </div>
                </div>
              </div>

              <div class="scan-image-wrapper">
                <!--
                  You can replace this placeholder with a real image:
                  <img src="your-image-here.jpg" alt="Sample face scan" />
                -->
                <div class="placeholder-img">
                  IMAGE PLACEHOLDER<br />
                  (Upload a portrait or content image here for scanning)
                </div>

                <div class="scan-tag">Detected Region: Face</div>
                <div class="scan-tag ai">AI Artifact Map</div>

                <div class="scan-score-bar">
                  <div class="score-labels">
                    <span>Real</span>
                    <span>|</span>
                    <span>AI</span>
                  </div>
                  <div class="score-bar-track">
                    <div class="score-real"></div>
                    <div class="score-ai"></div>
                  </div>
                  <div class="score-caption">Confidence: 55% real / 45% AI</div>
                </div>
              </div>
            </div>

            <!-- Right-hand side info -->
            <div class="hero-visual-side">
              <div class="hero-visual-pill">
                <strong>Key scan signals</strong>
                Micro-texture patterns, lighting consistency, and metadata traces are aggregated into a single
                authenticity score. Enigma Scanner visualizes why an image is flagged instead of producing a
                “black-box” verdict.
              </div>

              <div class="hero-visual-stats">
                <div class="hero-stat">
                  <div class="hero-stat-label">Avg. analysis time</div>
                  <div class="hero-stat-value">2.1 s</div>
                </div>
                <div class="hero-stat">
                  <div class="hero-stat-label">Signals combined</div>
                  <div class="hero-stat-value">32+</div>
                </div>
                <div class="hero-stat">
                  <div class="hero-stat-label">Explainability score</div>
                  <div class="hero-stat-value">92%</div>
                </div>
                <div class="hero-stat">
                  <div class="hero-stat-label">False-flag reduction</div>
                  <div class="hero-stat-value">38%</div>
                </div>
              </div>

              <div class="hero-visual-footer">
                <span>Prototype design for Group 8 | IT 304</span>
                <span class="badge">🔐 Focused on transparency &amp; user control</span>
              </div>
            </div>
          </div>

          <!-- Glowing blobs -->
          <div class="glow-blob one"></div>
          <div class="glow-blob two"></div>
        </div>
      </div>
    </section>

    <!-- ==========================
         FEATURES
         ========================== -->
    <section id="features">
      <div class="container">
        <h2>Core Capabilities of Enigma Scanner</h2>
        <p class="section-intro">
          Each module is designed to help you reason about authenticity instead of relying on a single
          “yes/no” prediction. You can customize the weights of each signal for different use cases.
        </p>

        <div class="feature-grid">
          <article class="feature-card">
            <div class="feature-tag">Module 01</div>
            <h3 class="feature-title">Pixel-Level Artifact Detection</h3>
            <p class="feature-text">
              Highlights subtle generative artifacts like repetitive textures, overly smooth skin,
              and inconsistent edges that are common in AI-generated content. Users see precisely
              which regions triggered the flag.
            </p>
            <div class="feature-meta">
              <span>Tech: frequency analysis, noise profiling</span>
              <span class="risk-chip">
                <span class="risk-dot risk-high"></span>
                High impact
              </span>
            </div>
          </article>

          <article class="feature-card">
            <div class="feature-tag">Module 02</div>
            <h3 class="feature-title">Metadata &amp; Provenance Checks</h3>
            <p class="feature-text">
              Inspects EXIF metadata, file history, and known AI generator signatures. While metadata
              can be removed, the scanner surfaces any available provenance hints and warns when
              information is missing.
            </p>
            <div class="feature-meta">
              <span>Tech: EXIF parsing, signature rules</span>
              <span class="risk-chip">
                <span class="risk-dot risk-medium"></span>
                Medium impact
              </span>
            </div>
          </article>

          <article class="feature-card">
            <div class="feature-tag">Module 03</div>
            <h3 class="feature-title">Context &amp; Consistency Analysis</h3>
            <p class="feature-text">
              Evaluates whether shadows, reflections, and proportions make sense together. This helps spot
              “uncanny” AI images that look real at first glance but break under closer inspection.
            </p>
            <div class="feature-meta">
              <span>Tech: geometric heuristics</span>
              <span class="risk-chip">
                <span class="risk-dot risk-medium"></span>
                Medium impact
              </span>
            </div>
          </article>

          <article class="feature-card">
            <div class="feature-tag">Module 04</div>
            <h3 class="feature-title">Explainable Scoring</h3>
            <p class="feature-text">
              Instead of a single percentage, the scanner breaks down the score into “signal bars”
              that show how each module contributed to the Real vs AI decision.
            </p>
            <div class="feature-meta">
              <span>Tech: weighted scoring model</span>
              <span class="risk-chip">
                <span class="risk-dot risk-low"></span>
                Low risk of mis-use
              </span>
            </div>
          </article>

          <article class="feature-card">
            <div class="feature-tag">Module 05</div>
            <h3 class="feature-title">Custom Profiles</h3>
            <p class="feature-text">
              Teachers, journalists, and security teams can define different profiles. For example,
              a “Classroom” profile might be more forgiving than a “Security Review” profile.
            </p>
            <div class="feature-meta">
              <span>Tech: adjustable threshold presets</span>
              <span class="risk-chip">
                <span class="risk-dot risk-low"></span>
                Low risk
              </span>
            </div>
          </article>

          <article class="feature-card">
            <div class="feature-tag">Module 06</div>
            <h3 class="feature-title">Privacy-Respecting Design</h3>
            <p class="feature-text">
              A future production version could run locally or on a secure server, ensuring that
              sensitive images do not need to be stored or shared unless the user chooses to.
            </p>
            <div class="feature-meta">
              <span>Tech: local processing option</span>
              <span class="risk-chip">
                <span class="risk-dot risk-low"></span>
                Privacy-focused
              </span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- ==========================
         HOW IT WORKS
         ========================== -->
    <section id="how-it-works">
      <div class="container">
        <h2>How a Scan Would Work</h2>
        <p class="section-intro">
          This is a conceptual flow showing how Enigma Scanner could operate in a real deployment. You can
          adapt these steps for class diagrams, system designs, or technical documentation.
        </p>

        <div class="timeline">
          <div class="timeline-step">
            <div class="timeline-number">01</div>
            <div class="timeline-content">
              <h3>Upload or paste the image</h3>
              <p>
                A user drags an image into the interface or pastes it from the clipboard.
                Enigma Scanner does an initial validation: file type, size limits, and basic metadata
                are inspected before deeper analysis starts.
              </p>
            </div>
          </div>

          <div class="timeline-step">
            <div class="timeline-number">02</div>
            <div class="timeline-content">
              <h3>Run analysis modules in parallel</h3>
              <p>
                The scanner runs pixel-level checks, metadata inspection, and contextual analysis in
                parallel to keep the experience fast. Each module outputs its own score and explanation.
              </p>
            </div>
          </div>

          <div class="timeline-step">
            <div class="timeline-number">03</div>
            <div class="timeline-content">
              <h3>Aggregate scores into one view</h3>
              <p>
                Scores are combined into a single Real vs AI bar, with separate breakdowns shown for transparency.
                Users can click into modules to see why certain artifacts were detected.
              </p>
            </div>
          </div>

          <div class="timeline-step">
            <div class="timeline-number">04</div>
            <div class="timeline-content">
              <h3>Review, document, and export</h3>
              <p>
                Finally, the user can download a short report summarizing key findings. This is useful for
                academic integrity cases, security investigations, or internal documentation.
              </p>
            </div>
          </div>
        </div>

        <!-- REAL VS AI IMAGE STRIP -->
        <div class="image-strip">
          <div class="image-strip-text">
            <h3>Visualizing Real vs AI Examples</h3>
            <p>
              Below are conceptual examples showing how Enigma Scanner might highlight differences
              between authentic and AI-generated content. Replace the placeholders with your own demo
              images if you’d like to make this interactive for a presentation.
            </p>
            <ul>
              <li><strong>Real image:</strong> natural imperfections, noise, and lighting inconsistencies.</li>
              <li><strong>AI image:</strong> overly sharp eyes, warped text, and “plastic” skin textures.</li>
              <li><strong>Heatmap overlay:</strong> highlights where the model is least confident.</li>
            </ul>
          </div>

          <div class="image-strip-gallery">
            <!-- Real photo example -->
            <div class="image-card">
              <div class="image-card-label">Real sample</div>
              <!-- Replace with a real photo URL -->
              <div class="placeholder-img">
                REAL IMAGE PLACEHOLDER<br />
                (e.g., unedited photo from a camera)
              </div>
              <div class="image-card-footer">
                <strong>Authentic reference</strong>
                Subtle imperfections and natural noise give the model higher confidence that
                this is likely human-captured content.
              </div>
            </div>

            <!-- AI portrait example -->
            <div class="image-card">
              <div class="image-card-label ai">AI-generated sample</div>
              <!-- Replace with an AI-generated portrait -->
              <div class="placeholder-img">
                AI IMAGE PLACEHOLDER<br />
                (e.g., face generated by a diffusion model)
              </div>
              <div class="image-card-footer">
                <strong>AI portrait indicators</strong>
                Eye reflections, hair strands, and jewelry often display subtle artifacts or impossible
                patterns.
              </div>
            </div>

            <!-- Heatmap overlay example -->
            <div class="image-card">
              <div class="image-card-label">Artifact heatmap</div>
              <div class="placeholder-img">
                HEATMAP PLACEHOLDER<br />
                (overlay showing high-risk regions in red)
              </div>
              <div class="image-card-footer">
                <strong>Risk regions</strong>
                Warm colors show where the scanner sees the strongest AI-like patterns.
              </div>
            </div>

            <!-- Report view example -->
            <div class="image-card">
              <div class="image-card-label">Report snapshot</div>
              <div class="placeholder-img">
                REPORT UI PLACEHOLDER<br />
                (summary of detection results with scores)
              </div>
              <div class="image-card-footer">
                <strong>Decision support</strong>
                The report is designed to be used alongside human judgment, not to automatically
                punish or approve content.
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==========================
         FAQ / LIMITATIONS
         ========================== -->
    <section id="faq">
      <div class="container">
        <h2>FAQ &amp; Limitations</h2>
        <p class="section-intro">
          No AI detection system is perfect. Enigma Scanner is designed to support human decisions,
          not replace them. These questions can guide classroom conversations about ethics, policy,
          and technical tradeoffs.
        </p>

        <div class="faq-grid">
          <article class="faq-item">
            <h3>Can Enigma Scanner be 100% certain?</h3>
            <p>
              No. AI models are constantly evolving, and some generated content will look extremely realistic.
              The tool outputs likelihoods, not guarantees. Results should always be combined with context and
              human review.
            </p>
          </article>

          <article class="faq-item">
            <h3>How could this help in a classroom?</h3>
            <p>
              Instructors might use Enigma Scanner as a teaching tool: to show how AI content is created,
              to discuss academic integrity, and to encourage transparent conversations about when AI tools
              are allowed or not.
            </p>
          </article>

          <article class="faq-item">
            <h3>What about privacy and data security?</h3>
            <p>
              A production version should clearly explain where images are stored, who can access them, and how
              long they are retained. A privacy-by-design approach would favor local analysis where possible.
            </p>
          </article>

          <article class="faq-item">
            <h3>Could detections be biased?</h3>
            <p>
              Yes. If trained on limited datasets, detectors can behave differently on certain types of images
              or populations. Regular audits, diverse training data, and human oversight are essential.
            </p>
          </article>
        </div>
      </div>
    </section>
  </main>

  <!-- ==========================
       FOOTER / AUTHORS
       ========================== -->
  <footer>
    <div class="container footer-inner">
      <div class="author-section">
        <strong>Author Section</strong>
        <div class="author-names">
          <span class="author-pill">Cameron</span>
          <span class="author-pill">Ali</span>
          <span class="author-pill">Lorenzo</span>
        </div>
      </div>

      <div>
        <div>Enigma Scanner • Group 8 IT 304</div>
        <div>Conceptual AI authenticity scanner for academic and security use cases.</div>
      </div>
    </div>
  </footer>
</body>
</html>
