<template>

 <h1>Dc hero</h1>
    <ul>
       <li v-for="(hero, index) in dcHeros" :key="index">
          {{ hero.name }}
       </li>
    </ul>

    <form @submit.prevent="dcHeros.push({ name: newHero });
    newHero='';
    "
    >
       <input v-model="newHero" placeholder="Type Hero Name here" />
       <button type="submit">Add Hero</button>
    </form>

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
