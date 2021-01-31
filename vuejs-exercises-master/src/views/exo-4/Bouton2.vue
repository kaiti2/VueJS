<template>
  <div>
    <button :class="{ yellow: yellow, thee: thee }" @click="submit">
      <slot>Envoyer</slot>{{ title }}
    </button>
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
    yellow: {
      type: Boolean,
      required: true,
    },
    thee: {
      type: Boolean,
      required: true,
    },
  },
  methods: {
    submit() {
      alert("Hello !");
    },
  },
};
</script>

<style>
.yellow {
  background: rgb(214, 218, 29);
  border: red 2px solid;
  border-radius: 50px;
  color: rgb(138, 101, 101);
}

.thee {
  background: rgb(14, 228, 50);
  border: rgb(156, 156, 194) 10px solid;
  border-radius: 80px;
  color: black;
}
</style>