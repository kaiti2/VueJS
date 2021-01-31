<template>
  <div class="exercise-2">       
    <div v-for="(contact, index) in users" :key="contact.id">
        
      <div :class="{isPremium: contact.premium}">       
        <p>{{contact.id}}</p>
        <img :src="image" alt="une image"/>
        <p>{{contact.firstname}}.{{contact.lastname}}</p> 
        <p>{{contact.email}}</p>
        <p>{{contact.password}}</p>

        <div :class="{isPremium:contact.premium}">
        <p>Etes vous Prémium?</p>
        <div class="premium">        
        <button @click="premium(index)">Prémium</button>
        <button @click="customEvent">Event</button>        
        </div>
          
        </div>
      </div>
    <div>

    </div>
    </div>  
  </div>


</template>
<script>
import {users} from './data.js'
export default {
  name: "Exercise2",
  data(){
    return {
      users:users,
      contact: [],
      isPremium: true,
      }
  },
  methods: {
  premium(index){
    this.users[index].premium = !this.users[index].premium;
  },
  customEvent(){
    this.$emit("event-name", {message: "Vous etes premium" })
  }
},
  computed:{ image () {
    return 'https://picsum.photos/200/300'
  }}
};

</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-2 {
  color: $grey;
}
.isPremium {
  background: blue;

}

</style>
