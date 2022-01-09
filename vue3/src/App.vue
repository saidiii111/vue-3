<template>
<div class="m-auto">
 <h1 class="text-3xl text-center my-4">Dc Hero {{ herosCount }}</h1>
    <ul class="border rounded p-2">
       <li class="flex justify-between" 
       v-for="(hero, index) in dcHeros" 
       :key="hero.name"
       >
          <div>
            {{ hero.name }}
          </div>
             <button
             class="border rounded bg-gradient-to-r from-red-700 to-pink-500 text-white ml-2 px-2" v-on:click="remove(index)">X</button>
        </li>
    </ul>

    <form class="mt-10"
     @submit.prevent="addHero">
       <input
       class="border rounded px-2"
        v-model.trim="newHero" placeholder="Type Hero Name here" />
       <button class="bg-info" type="submit">Add Hero</button>
    </form>
    </div>
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
