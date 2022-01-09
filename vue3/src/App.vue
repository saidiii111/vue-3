<template>

 <h1>Dc hero</h1>
    <ul>
     <li v-for="(hero, index) in dcHeros" :key="index">
       {{ index }} : {{ hero.name }}
       </li>
    </ul>
    <input v-model.number="newHero" />
    <button>Add Hero</button>
</template>


<script>
export default {
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
        }   ;
 },
};
</script>

<style>
body{
  background: #004400;
}
</style>
