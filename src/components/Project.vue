<template>
  <div class="project">
  <Logo/>
  <div class="main">
    <h1>{{data.titre}}</h1>
    <span>{{data.info}}</span>

    <div class="first">
      <img :src="getImgUrl(data.photo1)">
      <div class="content">
        <h2>{{data.titre1}}</h2>
        <p>{{data.paragraphe1}}</p>
      </div>
    </div>

    <div  v-if="data.couleurs" class="harmonie">
        <div :style="circle" class="cricle"></div>
        <div :style="circle2" class="cricle"></div>
        <div :style="circle3" class="cricle"></div>
        <div v-if="data.couleurs.c4" :style="circle4" class="cricle"></div>
    </div>

  <div class="background">
    <div class="second">
      <div class="content">
        <h2>{{data.titre2}}</h2>
        <p>{{data.paragraphe2}}</p>
        <p  v-if="data.paragraphe2bis">{{data.paragraphe2bis}}</p>
      </div>
      <img :src="getImgUrl(data.photo2)">
    </div>

    <Back/>
  </div>  </div>


    
  </div>
</template>

<script>
import data from '@/data/ENprojects.json'
import Back from '@/components/Back.vue'
import Logo from '@/components/Logo.vue'

export default {
  name: 'Project',
  components: {
    Back,
    Logo
  },
   data() {
      return {
          nom:'',
          data
      }
     },

     methods:{
       getImgUrl(pic) {
        return require('../assets/images'+ pic)
      }
     },

  mounted(){
    this.nom = this.$route.params.nom
    this.data = this.data[this.nom]

     var element = document.querySelector("body");
    element.removeAttribute("class");
    element.classList.add("bgVisible");
  },

  computed: {
    circle() {
      return {
        "background-color": this.data.couleurs.c1,
      };
    },

    circle2() {
      return {
        "background-color": this.data.couleurs.c2,
      };
    },

    circle3() {
      return {
        "background-color": this.data.couleurs.c3,
      };
    },

    circle4() {
      return {
        "background-color": this.data.couleurs.c4,
      };
    }
  }


}
</script>
<style scoped>
 .bgVisible{
    background-color: white;
      overflow: visible;
  }
.main{
  padding-top: 1px;
}
.cricle{
    width:80px;
    height:80px;
    border-radius:50%;
    margin:10px auto;
   }

   h1{
    background-color: black;
    font-size: 25px;
    text-align: center;
    width: 300px;
    color: white;
    font-weight: normal;
    display: block;
    margin: auto;
    padding: 5px;
    margin-top: 100px;
}

span{
    text-align: center;
    display: block;
    margin: 10px auto 0 auto;
}

.content{
  width: 45%;
}

   .first{
       display: flex;
       margin: 100px auto 0 auto;
       width: 50%;
       max-width: 900px;
       min-width: 600px;
       justify-content: space-between;
   }

   .first img{
       transform: rotate(-20deg);
       max-height: 300px;
   }

   .first p{
     text-align: left;
   }

   .first h2{
       text-align: right;
   }

   .harmonie{
       display: flex;
       margin: 150px auto 150px auto;
       width: 70%;
   }

   .background{
       background-color: #fafafa;
       width: 100%;
   }

   .second img{
    width: 50%;
    height: auto;
   }

   
   .second{
       display: flex;
       margin: 100px auto 0 auto;
       padding: 100px 0 0 0;
       width: 70%;
       max-width: 1200px;
       min-width: 900px;
       justify-content: space-between;
       text-align: left;
   }

   .second .content{
     width: 45%;
     margin-top: 40px;
   }


  

</style>
