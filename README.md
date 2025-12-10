/* =============== BASE =============== */
*,
*::before,
*::after {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: "Montserrat", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  background: #070709;
  color: #f6f2e9;
  line-height: 1.6;
}

img {
  max-width: 100%;
  display: block;
}

a {
  color: inherit;
  text-decoration: none;
}

.container {
  width: 100%;
  max-width: 1120px;
  padding: 0 1.5rem;
  margin: 0 auto;
}

/* =============== HEADER =============== */
.site-header {
  position: sticky;
  top: 0;
  z-index: 999;
  background: rgba(7, 7, 9, 0.9);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid rgba(255, 184, 76, 0.2);
}

.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.75rem 0;
}

.logo-wrap {
  display: flex;
  align-items: center;
  gap: 0.6rem;
}

.logo-img {
  width: 40px;
  height: 40px;
  border-radius: 999px;
}

.logo-text {
  font-weight: 700;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  font-size: 0.9rem;
  color: #ffb84c;
}

.main-nav {
  display: flex;
  gap: 1.5rem;
  font-size: 0.9rem;
}

.main-nav a {
  position: relative;
  padding-bottom: 0.25rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  font-weight: 500;
  color: #f6f2e9;
}

.main-nav a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, #ffb84c, #ff7b2c);
  transition: width 0.2s ease-out;
}

.main-nav a:hover::after {
  width: 100%;
}

/* Mobile nav button */
.nav-toggle {
  display: none;
  width: 36px;
  height: 32px;
  border: none;
  background: transparent;
  padding: 0;
  cursor: pointer;
}

.nav-toggle span {
  display: block;
  height: 2px;
  background: #f6f2e9;
  margin: 6px 0;
  transition: transform 0.25s ease, opacity 0.25s ease;
}

/* =============== HERO =============== */
.hero-section {
  padding: 4.5rem 0 4rem;
  background: radial-gradient(circle at top, #262021 0, #070709 55%);
}

.hero-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 3rem;
  flex-wrap: wrap;
}

.hero-text h1 {
  font-size: 2.8rem;
  margin: 0 0 0.75rem;
  background: linear-gradient(90deg, #ffb84c, #ff7b2c);
  -webkit-background-clip: text;
  color: transparent;
}

.hero-subtitle {
  max-width: 480px;
  color: #d9d3c7;
  margin-bottom: 1.5rem;
}

.hero-cta {
  display: flex;
  gap: 1rem;
  margin-bottom: 1rem;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.75rem 1.6rem;
  border-radius: 999px;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  font-size: 0.8rem;
  border: 1px solid transparent;
  cursor: pointer;
  transition: transform 0.12s ease-out, box-shadow 0.12s ease-out, background 0.12s ease-out;
}

.primary-btn {
  background: linear-gradient(135deg, #ffb84c, #ff7b2c);
  color: #070709;
  box-shadow: 0 8px 24px rgba(255, 145, 46, 0.35);
}

.primary-btn:hover {
  transform: translateY(-1px);
  box-shadow: 0 12px 28px rgba(255, 145, 46, 0.5);
}

.outline-btn {
  border-color: rgba(255, 184, 76, 0.7);
  color: #ffb84c;
  background: transparent;
}

.outline-btn:hover {
  background: rgba(255, 184, 76, 0.1);
}

.hero-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag {
  padding: 0.3rem 0.7rem;
  border-radius: 999px;
  border: 1px solid rgba(255, 184, 76, 0.4);
  font-size: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: #e3ddcf;
}

.hero-image {
  flex: 0 0 280px;
  max-width: 320px;
  margin-left: auto;
}

.hero-image img {
  filter: drop-shadow(0 18px 40px rgba(0, 0, 0, 0.9));
}

/* =============== SECTIONS GENERIC =============== */
.section {
  padding: 4rem 0;
}

.section h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.section-intro {
  max-width: 600px;
  color: #d0c8b9;
  margin-bottom: 2rem;
}

/* Layout helpers */
.two-col {
  display: grid;
  grid-template-columns: minmax(0, 2fr) minmax(0, 1.3fr);
  gap: 2.5rem;
  align-items: flex-start;
}

/* Cards and info blocks */
.info-card {
  background: radial-gradient(circle at top left, rgba(255, 184, 76, 0.15), rgba(9, 10, 18, 0.95));
  border-radius: 1.4rem;
  padding: 1.75rem 1.6rem;
  border: 1px solid rgba(255, 184, 76, 0.25);
}

.info-card h3 {
  margin-top: 0;
  margin-bottom: 1rem;
  font-size: 1.1rem;
}

.info-card ul {
  list-style: none;
  padding-left: 1rem;
  margin: 0;
}

.info-card li {
  margin-bottom: 0.6rem;
  position: relative;
}

.info-card li::before {
  content: "•";
  position: absolute;
  left: -0.9rem;
  color: #ffb84c;
}

/* =============== TOKENOMICS =============== */
.tokenomics-section {
  background: radial-gradient(circle at center, #171218 0, #070709 55%);
}

.tokenomics-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.token-card {
  background: rgba(14, 12, 16, 0.98);
  border-radius: 1.25rem;
  padding: 1.4rem 1.3rem;
  border: 1px solid rgba(255, 184, 76, 0.2);
}

.token-card h3 {
  margin: 0 0 0.5rem;
  font-size: 1rem;
}

.token-value {
  margin: 0 0 0.3rem;
  font-weight: 700;
  color: #ffb84c;
}

.token-note {
  margin: 0;
  font-size: 0.85rem;
  color: #cbbfae;
}

.disclaimer {
  margin-top: 1.8rem;
  font-size: 0.8rem;
  color: #a79c8b;
}

/* =============== ROADMAP =============== */
.roadmap-timeline {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.75rem;
  margin-top: 2rem;
}

.roadmap-item {
  position: relative;
  padding: 1.6rem 1.4rem;
  border-radius: 1.4rem;
  background: linear-gradient(135deg, rgba(255, 184, 76, 0.16), rgba(9, 9, 15, 0.98));
  border: 1px solid rgba(255, 184, 76, 0.35);
}

.roadmap-phase {
  display: inline-block;
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-bottom: 0.4rem;
  color: #ffdd9a;
}

.roadmap-item h3 {
  margin: 0 0 0.6rem;
}

.roadmap-item ul {
  padding-left: 1.1rem;
  margin: 0;
  font-size: 0.9rem;
}

/* =============== HOW TO BUY =============== */
.how-section {
  background: #060509;
}

.steps-list {
  counter-reset: steps;
  margin: 0;
  padding-left: 0;
  list-style: none;
}

.steps-list li {
  position: relative;
  margin-bottom: 1rem;
  padding-left: 2.4rem;
  font-size: 0.95rem;
}

.steps-list li::before {
  counter-increment: steps;
  content: counter(steps);
  position: absolute;
  left: 0;
  top: 0.15rem;
  width: 1.6rem;
  height: 1.6rem;
  border-radius: 999px;
  border: 1px solid rgba(255, 184, 76, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.8rem;
  color: #ffb84c;
}

/* =============== COMMUNITY =============== */
.community-section {
  background: radial-gradient(circle at bottom, #1a1417 0, #070709 55%);
}

.social-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
  margin-top: 2rem;
}

.social-card {
  border-radius: 1.2rem;
  padding: 1rem 1.1rem;
  border: 1px solid rgba(255, 184, 76, 0.25);
  background: rgba(10, 9, 12, 0.95);
  transition: transform 0.12s ease-out, box-shadow 0.12s ease-out, border-color 0.12s ease-out;
}

.social-card:hover {
  transform: translateY(-2px);
  border-color: rgba(255, 184, 76, 0.8);
  box-shadow: 0 14px 30px rgba(0, 0, 0, 0.6);
}

.social-label {
  font-size: 0.75rem;
  text-transform: uppercase;
  letter-spacing: 0.16em;
  color: #ffdd9a;
}

.social-handle {
  display: block;
  margin-top: 0.3rem;
  font-weight: 600;
}

/* =============== FOOTER =============== */
.site-footer {
  border-top: 1px solid rgba(255, 184, 76, 0.2);
  background: #050406;
}

.footer-inner {
  padding: 1.5rem 0 1.8rem;
  text-align: center;
}

.footer-inner p {
  margin: 0.2rem 0;
}

.footer-note {
  font-size: 0.78rem;
  color: #9f9586;
}

/* =============== RESPONSIVE =============== */
@media (max-width: 900px) {
  .hero-inner {
    flex-direction: column-reverse;
    text-align: center;
  }

  .hero-text h1 {
    font-size: 2.3rem;
  }

  .hero-subtitle {
    margin-left: auto;
    margin-right: auto;
  }

  .hero-cta {
    justify-content: center;
  }

  .hero-tags {
    justify-content: center;
  }

  .two-col {
    grid-template-columns: minmax(0, 1fr);
  }
}

@media (max-width: 768px) {
  .main-nav {
    position: fixed;
    inset: 56px 0 auto 0;
    background: rgba(7, 7, 9, 0.98);
    flex-direction: column;
    padding: 1rem 1.5rem 1.5rem;
    transform: translateY(-120%);
    opacity: 0;
    pointer-events: none;
    transition: transform 0.25s ease-out, opacity 0.25s ease-out;
  }

  .main-nav.nav-open {
    transform: translateY(0);
    opacity: 1;
    pointer-events: auto;
  }

  .nav-toggle {
    display: block;
  }

  .nav-toggle.nav-open span:nth-child(1) {
    transform: translateY(8px) rotate(45deg);
  }

  .nav-toggle.nav-open span:nth-child(2) {
    opacity: 0;
  }

  .nav-toggle.nav-open span:nth-child(3) {
    transform: translateY(-8px) rotate(-45deg);
  }
}

@media (max-width: 480px) {
  .hero-section {
    padding-top: 3.2rem;
  }

  .hero-text h1 {
    font-size: 2rem;
  }

  .btn {
    width: 100%;
    justify-content: center;
  }

  .hero-cta {
    flex-direction: column;
  }
}
