<template>
  <div id="app">
      <router-view/>
  </div>
</template>

<script>
// import Logo from '@/components/Logo.vue'
export default {
//   components: {
//     Logo
//   }

mounted(){
    let isMobile = false;
     if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        isMobile = true;
  }
    this.$store.commit('device', isMobile);
}

 }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body{
  margin: 0;
}

@font-face {
    font-family: NotoSans;
    src:url(assets/fonts/Noto_Sans/NotoSans-Regular.ttf);
}

@font-face {
    font-family: NotoSansItalic;
    src:url(assets/fonts/Noto_Sans/NotoSans-Italic.ttf);
}

@font-face {
    font-family: NotoSansBold;
    src:url(assets/fonts/Noto_Sans/NotoSans-Bold.ttf);
}

@font-face {
    font-family: Questrial;
    src:url(assets/fonts/Questrial/Questrial-Regular.ttf);
}

h1,h2,h3{
    font-family: Questrial, sans-serif;
    font-weight: normal;
}

h2{
    font-size: 20px;
    letter-spacing: 3px;
}

h1{
    letter-spacing: 3px;
}

p,a{
    font-family: NotoSans, sans-serif;
    font-size: 14px;
}

span{
    font-family: NotoSansItalic, sans-serif;
}

</style>
