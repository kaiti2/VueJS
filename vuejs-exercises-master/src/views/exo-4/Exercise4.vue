<template>
  <div class="exercise-4">
    <div class="containt">
      <Bouton2 title="title"> S'enregistrer </Bouton2><br /><br />
      <Bouton2 title="Super" :yellow="true"></Bouton2><br /><br />
      <Bouton2 title="Succes" :thee="true" @click.native="titre"></Bouton2>

      <Card>
        <template v-slot:titre-carte>
          <h1>Ceci est le premier titre de la carte</h1>

          <h1>{{ title2 }}</h1>
        </template>

        <p>Bonjour, je suis le main</p>
        <template v-slot:paragraph>
          <p>Voici le paragraphe par défaut</p>
        </template>
      </Card>
    </div>
  </div>
</template>

<script>
import Bouton2 from "./Bouton2.vue";
import Card from "./Card.vue";
export default {
  name: "Exercise4",
  data() {
    return {
      title2: "Ceci est le nouveau titre",
    };
  },
  components: {
    Bouton2,
    Card,
  },
  methods: {
    titre: function () {
      this.title2 = "le dernier ";
    },
  },
};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-4 {
  color: $grey;
}

.containt {
  border: 3px solid red;
  color: blue;
}
</style>
