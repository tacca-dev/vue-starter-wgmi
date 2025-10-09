<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="site-layout">
    <header class="site-header">
      <RouterLink to="/" class="site-brand">
        <img alt="Vue logo" class="brand-logo" src="@/assets/logo.svg" width="48" height="48" />
        <span class="brand-text">Vue + Builder.io</span>
      </RouterLink>
      <nav class="site-navigation">
        <RouterLink class="navigation-link" to="/">Home</RouterLink>
        <RouterLink class="navigation-link" to="/about">About</RouterLink>
      </nav>
    </header>

    <main class="site-main">
      <RouterView />
    </main>
  </div>
</template>

<style scoped>
.site-layout {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.site-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1.5rem;
  padding: 1.25rem 1.5rem;
  border: 1px solid var(--color-border);
  border-radius: 18px;
  background: var(--color-background-soft);
  box-shadow: 0 12px 32px rgba(24, 24, 24, 0.08);
}

.site-brand {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-heading);
}

.brand-logo {
  border-radius: 14px;
  background: linear-gradient(135deg, rgba(76, 201, 240, 0.2), rgba(60, 220, 130, 0.2));
  padding: 0.4rem;
}

.brand-text {
  letter-spacing: 0.02em;
}

.site-navigation {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.navigation-link {
  padding: 0.5rem 0.9rem;
  border-radius: 12px;
  font-weight: 500;
  color: var(--color-text);
}

.navigation-link.router-link-exact-active {
  color: hsla(160, 100%, 37%, 1);
  background: hsla(160, 100%, 37%, 0.12);
}

.site-main {
  flex: 1;
}

@media (hover: hover) {
  .navigation-link:hover {
    background: rgba(24, 24, 24, 0.06);
  }
}

@media (prefers-color-scheme: dark) {
  .site-header {
    border: 1px solid rgba(255, 255, 255, 0.1);
    box-shadow: 0 12px 32px rgba(0, 0, 0, 0.6);
  }

  .navigation-link:hover {
    background: rgba(255, 255, 255, 0.1);
  }
}

@media (max-width: 640px) {
  .site-header {
    flex-direction: column;
    align-items: flex-start;
  }

  .site-navigation {
    width: 100%;
    justify-content: space-between;
  }
}
</style>
