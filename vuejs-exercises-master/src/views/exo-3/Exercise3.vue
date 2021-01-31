<template>
  <div class="exercise-3">
    <Bouton title="title" :hasError="false" :green="true" error="Une erreur c'est produite!"></Bouton>
    <Bouton title="true" :pink="true"></Bouton>
    <Bouton title="bouton3" :blue="true"></Bouton>
    </div>   
</template>

<script>
import Bouton from './Bouton.vue';
export default {
  name: "Exercise3",
  components: {
    Bouton,

  },

};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-3 {
  color: $grey;
}
</style>

