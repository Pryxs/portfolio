<template>
  <div class="projects">
    <Logo/>
    <div class="main">
    <h1>Mes projets</h1>
    <div id="liste">
    <div class="item" v-for="item in data" :key="item.nom" @click="viewProject(item)">
      <img :src="getImgUrl(item.miniature)">
      <h2>{{item.titre}}</h2>
    </div>
  </div>
  </div>
  </div>
</template>

<script>
import data from '@/data/ENprojects.json'
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
       },

       getImgUrl(pic) {
        return require('../assets/images'+ pic)
      }
     },

     mounted(){
    var element = document.querySelector("body");
    element.removeAttribute("class");
    element.classList.add("bgPro");
  }
}
</script>

<style scoped>
h1{
  margin-top: 40px;
}
  .bgPro{
    background-color: white;
      overflow: hidden;
  }

  h2{
    color: white;
    letter-spacing: 1px;
    opacity: 0;
  }

  .item:hover h2{
     transition: 0.3s;
    transform: translateY(-60px);
    opacity: 1;
  }

  .main{
    padding-top: 1px;
  }

  .item{
    margin: 5px 10px;
    height  : 250px;
  }

  .item img{
    border-radius: 15px;
  }

  #liste{
    display: flex;
    width: 100%;
    flex-wrap: wrap;
    justify-content: center;
  }

  @media (min-width: 1220px) {
    #liste{
       position: absolute;
      top: 55%;
      transform: translateY(-50%);
    }

  }



</style>
