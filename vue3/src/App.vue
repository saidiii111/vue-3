<template>
 <h1>Dc hero</h1>
    <ul>
     <li v-for="(hero, index) in dcHeros" v-bind:key="index">
       {{ index }} : {{ hero.name }}
       </li>
    </ul>
</template>


<script>
export default {
data(){
  return {
    dcHeros : [
     { name: "SuperGirl" },
     { name: "SuperGirl" },
     { name: "SuperGirl" },
     { name: "SuperGirl" },
     { name: "SuperGirl" },
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
