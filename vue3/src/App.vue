<template>

 <h1>Dc hero {{ herosCount }}</h1>
    <ul>
       <li v-for="(hero, index) in dcHeros" :key="index">
          <div>{{ hero.name }} <button v-on:click="remove(index)">X</button></div>
       </li>
    </ul>

    <form @submit.prevent="addHero">
       <input v-model.trim="newHero" placeholder="Type Hero Name here" />
       <button type="submit">Add Hero</button>
    </form>
</template>


<script>
export default {
  computed: {
     herosCount() {
   return this.dcHeros.length + ' Heros';
     },
  },
  methods:{
   addHero() {
     if(this.newHero !== "") {
     this.dcHeros.push({ name: this.newHero });
     this.newHero = "";
     }
   },
   remove(index) {
     this.dcHeros = this.dcHeros.filter((hero, i) => i != index); 
   },
  },
data(){  
  return {
    newHero: "AquaMan77",
    dcHeros : [
        { name: "SuperGirl" },
        { name: "Flash" },
        { name: "BatMan" },
        { name: "Arrow" },
        { name: "SuperMan" },  
              ],
        };
    },
 };

</script>
  


<style>
body{
  background: #004400;
}
</style>
