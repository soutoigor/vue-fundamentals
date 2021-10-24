<template>
  <section class="card">
    <header class="card__header">
      <h1>
        <slot name="header">
          Default card Title
        </slot>
      </h1>
    </header>
    <main class="card__content">
      <slot />
    </main>
    <footer class="card__footer">
      <slot name="footer" :anything="anyMethod" />
    </footer>
  </section>
</template>

<script>
export default {
  methods: {
    anyMethod() {
      alert('Alert!!! :D')
    },
  },
}
</script>

<style>
.card {
  border: 1px solid #000;
  padding: 2px;
  border-radius: 6px;
}

.card__header {
  font-style: italic;
}

.card__content {
  font-size: .9rem;
  font-weight: 600;
}

.card__footer {
  display: flex;
  justify-content: flex-end;
}
</style>
