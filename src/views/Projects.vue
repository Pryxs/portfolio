<template>
  <div class="projects">
    <Logo/>
    <h1>Mes projets</h1>
    <ul id="liste">
    <div class="item">
      <li v-for="item in data" :key="item.nom" @click="viewProject(item)">
        {{item.nom}}
      </li>
    </div>
  </ul>
  </div>
</template>

<script>
import data from '@/data/projects.json'
import Logo from '@/components/Logo.vue'

export default {
    name: 'projects',
    components: {
    Logo
  },

    data() {
      return {
          data,
          
      }
     },

     methods:{
       viewProject(event){
         this.$router.push({ name: 'projet', params: {nom: event.nom }})
       }
     },

     mounted(){
    var element = document.querySelector("body");
    element.removeAttribute("class");
    element.classList.add("bgPro");
  }
}
</script>

<style>
  .bgPro{
    background-color: white;
      overflow: hidden;
  }



</style>
