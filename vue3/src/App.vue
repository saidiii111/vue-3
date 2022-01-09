<template>

 <h1>Dc hero</h1>
    <ul>
     <li v-for="(hero, index) in dcHeros" :key="index">
       {{ index }} : {{ hero.name }}
       </li>
    </ul>
    <input :[attribute]="newHero" />
    <button :disabled="isDisabled">Add Hero</button>
</template>


<script>
export default {
data(){  
  return {
    attribute: "value",
    isDisabled: true,
    newHero: "AquaMan",
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
