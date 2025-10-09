<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="home-view">
    <section class="hero-banner">
      <div class="hero-message">
        <span class="hero-label">Modern front-end foundation</span>
        <h1 class="hero-heading">Welcome to Vue + Builder.io!</h1>
        <p class="hero-description">
          Craft composable experiences with Vue 3 while empowering teams to edit content visually in Builder.io.
        </p>
        <div class="hero-actions">
          <a class="primary-action" href="https://www.builder.io/" target="_blank" rel="noopener">Explore Builder.io</a>
          <RouterLink class="secondary-action" to="/about">Discover the stack</RouterLink>
        </div>
      </div>
      <div class="hero-showcase">
        <div class="showcase-card">
          <h2 class="showcase-title">Build, iterate, and ship visually</h2>
          <p class="showcase-text">
            Drag-and-drop sections, sync with your Vue components, and ship updates without redeploying.
          </p>
          <ul class="showcase-list">
            <li>Reusable content models and targeting</li>
            <li>Live previews with your component library</li>
            <li>Performance optimized for production</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="feature-section">
      <h2 class="section-heading">Why this starter stands out</h2>
      <div class="feature-grid">
        <article class="feature-tile">
          <h3 class="tile-title">Composable architecture</h3>
          <p class="tile-description">
            Structure your UI with Vue 3’s composition API and keep layouts flexible for future growth.
          </p>
        </article>
        <article class="feature-tile">
          <h3 class="tile-title">Visual content control</h3>
          <p class="tile-description">
            Let marketing teams create campaigns directly in Builder.io while engineers stay focused on core product work.
          </p>
        </article>
        <article class="feature-tile">
          <h3 class="tile-title">Optimized delivery</h3>
          <p class="tile-description">
            Ship fast with Vite’s lightning build pipeline and edge-ready assets served wherever your users are.
          </p>
        </article>
      </div>
    </section>
  </div>
</template>

<style scoped>
.home-view {
  display: flex;
  flex-direction: column;
  gap: 3.5rem;
  padding-bottom: 3rem;
}

.hero-banner {
  display: grid;
  gap: 2.5rem;
  padding: 3rem;
  border-radius: 28px;
  border: 1px solid var(--color-border);
  background: linear-gradient(135deg, rgba(76, 201, 240, 0.2), rgba(60, 220, 130, 0.15));
  position: relative;
  overflow: hidden;
}

.hero-banner::after {
  content: '';
  position: absolute;
  inset: auto -30% -30% 40%;
  height: 320px;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.35), transparent 70%);
  pointer-events: none;
}

.hero-message {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  max-width: 520px;
  z-index: 1;
}

.hero-label {
  align-self: flex-start;
  padding: 0.25rem 0.85rem;
  border-radius: 999px;
  font-size: 0.85rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  background: rgba(24, 24, 24, 0.08);
  color: var(--color-heading);
}

.hero-heading {
  font-size: clamp(2.5rem, 5vw, 3.4rem);
  font-weight: 700;
  color: var(--color-heading);
  line-height: 1.1;
}

.hero-description {
  font-size: 1.05rem;
  color: var(--color-text);
  max-width: 480px;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.primary-action {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.75rem 1.5rem;
  border-radius: 14px;
  font-weight: 600;
  background: hsla(160, 100%, 37%, 1);
  color: var(--color-background);
  box-shadow: 0 12px 30px rgba(24, 24, 24, 0.18);
}

.secondary-action {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.75rem 1.5rem;
  border-radius: 14px;
  font-weight: 600;
  border: 1px solid rgba(24, 24, 24, 0.2);
  color: var(--color-heading);
  background: rgba(255, 255, 255, 0.6);
  backdrop-filter: blur(6px);
}

.hero-showcase {
  display: flex;
  justify-content: flex-end;
  z-index: 1;
}

.showcase-card {
  max-width: 360px;
  padding: 2rem;
  border-radius: 24px;
  border: 1px solid rgba(24, 24, 24, 0.08);
  background: rgba(255, 255, 255, 0.9);
  box-shadow: 0 20px 40px rgba(24, 24, 24, 0.16);
  backdrop-filter: blur(10px);
}

.showcase-title {
  font-size: 1.35rem;
  font-weight: 600;
  color: var(--color-heading);
  margin-bottom: 0.75rem;
}

.showcase-text {
  color: var(--color-text);
  margin-bottom: 1rem;
  line-height: 1.6;
}

.showcase-list {
  display: grid;
  gap: 0.6rem;
  padding-left: 1.2rem;
  color: var(--color-text);
}

.feature-section {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.section-heading {
  font-size: 2rem;
  font-weight: 600;
  color: var(--color-heading);
}

.feature-grid {
  display: grid;
  gap: 1.5rem;
}

.feature-tile {
  padding: 1.75rem;
  border-radius: 20px;
  border: 1px solid var(--color-border);
  background: var(--color-background-soft);
  box-shadow: 0 10px 24px rgba(24, 24, 24, 0.08);
  transition: transform 0.3s ease;
}

.feature-tile:hover {
  transform: translateY(-6px);
}

.tile-title {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-heading);
  margin-bottom: 0.75rem;
}

.tile-description {
  color: var(--color-text);
  line-height: 1.6;
}

@media (min-width: 768px) {
  .hero-banner {
    grid-template-columns: minmax(0, 1fr) minmax(0, 0.9fr);
    align-items: center;
  }

  .feature-grid {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}

@media (max-width: 480px) {
  .hero-banner {
    padding: 2.25rem;
  }

  .showcase-card {
    padding: 1.75rem;
  }
}

@media (prefers-color-scheme: dark) {
  .hero-banner {
    background: linear-gradient(135deg, rgba(76, 201, 240, 0.15), rgba(88, 101, 242, 0.18));
  }

  .hero-label {
    background: rgba(255, 255, 255, 0.16);
  }

  .secondary-action {
    border: 1px solid rgba(255, 255, 255, 0.35);
    background: rgba(24, 24, 24, 0.7);
    color: var(--color-text);
  }

  .showcase-card {
    background: rgba(24, 24, 24, 0.75);
    border: 1px solid rgba(255, 255, 255, 0.12);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.55);
  }

  .feature-tile {
    background: rgba(24, 24, 24, 0.7);
    border: 1px solid rgba(255, 255, 255, 0.1);
    box-shadow: 0 10px 28px rgba(0, 0, 0, 0.55);
  }
}
</style>
