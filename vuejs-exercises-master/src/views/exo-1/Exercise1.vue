<template>
  <div class="exercise-1">
    <h1>Bienvenue {{ firstname + " " + lastname }} !</h1>
    <label for="name">Prénom :</label>
    <input type="text" v-model="texte" /><br /><br />

    <label for="name">Age :</label>
    <input type="number" v-model="age" />
    <p v-if="age === ''"></p>
    <p v-else-if="age > 18">{{ texte }}, vous avez plus de 18 ans</p>
    <p v-else-if="age == 18">{{ texte }}, vous avez 18 ans</p>
    <p v-else-if="age < 18">{{ texte }}, vous avez moins de 18 ans</p>

    <p v-if="age !== ''">vous etes née en {{ year - age }}</p>
  </div>
</template>

<script>
export default {
  name: "Exercise1",
  data() {
    return {
      firstname: "Anne",
      lastname: "Trotreau",
      texte: "",
      age: "",
      year: 2021,
    };
  },
};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-1 h1 {
  color: $grey;
}
</style>