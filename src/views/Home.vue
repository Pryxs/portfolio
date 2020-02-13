<template>
  <div class="home">
    <div class="logo">
            <router-link to="/">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="100 100 652.38 652.38">
                    <title>logo</title>
                    <g id="logo" data-name="logo"><polyline class="cls-6" points="372.24 478.38 341.14 440.78 384.68 440.78 415.78 478.38 372.24 478.38"/>
                    <path class="cls-6" d="M322.14,177.1c24.88,0,93.3,12.44,93.3,93.3s-65.44,91-99.44,91H230l14-27.92s58.63-.09,72-.08c27,0,68.34-13.22,68.34-63,0-43.54-37.34-62-66.34-62-1,0-11.41-.18-11.41-.18Z"/></g>
                    </svg>
            </router-link>
        </div>
        <div class="presentation">
          <h1>Corentin Roy</h1>
          <h1>Développeur Web</h1>
          <p>Salut salut ! Moi c'est Corentin, un étudiant dans les métiers du numérique et plus particulièrement en développement web. Je cherche un stage qui débutera mi-avril alors si vous appréciez mon travail <a href="mailto:corentin25200@gmail.com">contactez-moi</a> ;)</p>
        </div>
    <Social/>
    <Navigation/>
  </div>
</template>

<script>
// @ is an alias to /src
import Social from '@/components/Social.vue'
import Navigation from '@/components/Navigation.vue'

export default {
  name: 'home',
  components: {
    Social,
    Navigation
  },
  

  mounted(){
    var element = document.querySelector("body");
    element.removeAttribute("class");
    element.classList.add("bg");
  }
}
</script>

<style>
.cls-6{fill:white;stroke:white;stroke-width:1px;}

.presentation{
  width: 770px;
  display: block;
  position: absolute;
  margin: auto;
  top: 40%;
  left: 50%; 
  transform: translate(-50%, -50%);
  color: #f4f4f4

}

.presentation h1{
    letter-spacing: 0.5px;
    font-family: NotoSans;
  font-size: 55px;
  margin: 0;
    text-align: right;
}

.presentation p{
  margin-top: 70px;
  width: 80%;
}

.presentation a{
  color: #F2BCB8;
}

.presentation h1:nth-child(2){
  font-size: 70px;
  text-align: center;
  background-image: linear-gradient(120deg, #EF9597 0%, #F2BCB8 100%);
  background-repeat: no-repeat;
  background-size: 50% 0.2em;
  background-position: 40px 88%;
  transition: background-size 0.25s ease-in;
}

.presentation h1:nth-child(2):hover{
      background-size: 490px 88%;
}

.presentation h1:first-child::before{
    content: ". ";
  color: #EF9597;
  font-size: 80px;
}

.logo{
    width: 80px;
    padding: 20px 0 0 20px;
}

.logo *{
    transition: 0.3s;
}
.logo:hover .cls-6
{
    animation-duration: 0.3s;
    stroke-width: 10px;
    transform: translate(20px,20px);

}

.bg{
  background-color: #4682B4;
  overflow: hidden;
}
  .social{
    position: absolute;
    width: 75px;
    top: 55%;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 50%;


}

</style>
