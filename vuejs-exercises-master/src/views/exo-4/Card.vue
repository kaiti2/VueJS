<template>
  <div class="card">
    <header>
      <slot name="titre-carte"></slot>
    </header>
    <main>
      <slot>Envoyer</slot>
    </main>
    <footer>
      <slot name="paragraph"></slot>
    </footer>
  </div>
</template>

<script>
export default {
  name: "Bouton2",
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>