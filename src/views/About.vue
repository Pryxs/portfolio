<template>
    <div class="about">
        <div class="logo">
        <router-link to="/">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="100 100 652.38 652.38">
                <title>logo</title>
                <g id="logo" data-name="logo"><polyline class="cls-5" points="372.24 478.38 341.14 440.78 384.68 440.78 415.78 478.38 372.24 478.38"/>
                <path class="cls-5" d="M322.14,177.1c24.88,0,93.3,12.44,93.3,93.3s-65.44,91-99.44,91H230l14-27.92s58.63-.09,72-.08c27,0,68.34-13.22,68.34-63,0-43.54-37.34-62-66.34-62-1,0-11.41-.18-11.41-.18Z"/></g>
                </svg>
        </router-link>
    </div>

      <div class="cont">
        <h1>A propos</h1>
            <div class="main">
            <div class="content">
                <h2>Corentin Roy,</h2>
                <h3>Etudiant en <a href="https://iut-charlemagne.univ-lorraine.fr/informatique/lp-informatique-ciasie/">LP CIASIE à Nancy</a></h3>
                <p>Passionné d'informatique et de dessin j'aime associer cette créativité avec la programmation. 
                    Créer est programmé sont au centre de mes activités. J'aime résoudre des problèmes dont je 
                    n'ai intuitivement aucune réponse, c'est cette perspective d'évolution qui m'attire dans ce 
                    domaine.  </p>
            </div>
            <img src="../assets/corentin_roy.png">
            </div>
            <div class="svg-wrapper">
                    <svg height="40" width="200" xmlns="http://www.w3.org/2000/svg">
                      <rect class="shape" height="40" width="200" />
                    </svg>
            <a href="CurriculumVitae_CorentinRoy.pdf" class="but" download title="téléchargement" >Mon CV</a>
            </div>
            </div>
    </div>
</template>

<script>

export default {
  name: 'About',
 
   mounted(){
    var element = document.querySelector("body");
    element.removeAttribute("class");
    element.classList.add("bgPro");
  }

}
</script>

<style scoped>
.cont{
  position: absolute;
  top: 50%;
  left: 50%; 
  transform: translate(-50%, -50%);
}

.bgPro {
    height: 100%;  
    overflow: hidden;
}

h1{
    background-color: black;
    font-size: 25px;
    text-align: center;
    width: 230px;
    color: white;
    font-weight: normal;
    display: block;
    margin:  10px auto;
    padding: 5px;
}

.main{
    display: flex;
    width: 700px;
    margin: 20px auto 50px auto;
    padding-bottom: 15px;
}

img{
    width: auto;
    height: 200px;
    margin-top: 50px;
}

h2,h3{
    text-align: right;

}

.content{
    margin-right: 50px;
    margin-top: 50px;
}

h2{
    font-size: 22px;
}

h3{
    font-size: 18px;
}

p{
    font-size: 16px;
    text-align: left;
}

h3 a{
    color: black;
}

@media (max-width: 768px) {
    main{
        display: block;
        width: 100%;
        
    }

    .contenu{
        margin: 50px;
        margin-top: 70px;
    }

    img{
        display: block;
        margin: auto;
    }



}
.svg-wrapper {
    height: 40px;
      margin: 0 auto;
    position: relative;
    top: 50%;
    transform: translateY(-50%);
    width: 200px;
    margin-top: 100px;
  }
  
  .shape {
    fill: transparent;
    stroke-dasharray: 31 87;
    stroke-dashoffset: -542;
    stroke-width: 2px;
    stroke: black;
    width: 200px;
    height: 40px;
  
  }
  
  .text {
    color: black;
    font-family: 'Questrial';
    font-size: 22px;
    letter-spacing: 8px;
    line-height: 32px;
    position: relative;
    top: -48px;
  }
  
  @keyframes draw {
    0% {
      stroke-dasharray: 72 114;
      stroke-dashoffset: -542;
    }
  
    70%{
      stroke-dashoffset: -114;
      stroke-width: 3px;
  
  
    }
    100% {
      stroke-dasharray: 800 0;
      stroke-dashoffset: 0;
      stroke-width: 2px;
    }
  }
  
  .svg-wrapper:hover .shape {
    -webkit-animation: 0.8s draw linear forwards;
    animation: 0.8s draw linear forwards;
  }

  .but{
    display: block;
    margin: auto;
    background-color: transparent;
    border: solid 1px black; 
    height: 40px;
    width: 120px;
    border: none;
    position: relative;
    top: -32px;
    text-align: center;
    font-family: Questrial, sans-serif;
    letter-spacing: 3px;
    cursor: pointer;
    font-size: 16px;
    text-decoration: none;
    color: black;
  }

  .cls-5{fill:black;stroke:black;stroke-width:1px;}


  .logo{
    width: 80px;
    padding: 20px 0 0 20px;
    position: fixed;
}

.logo *{
    transition: 0.3s;
}
.logo:hover .cls-5
{
    animation-duration: 0.3s;
    stroke-width: 10px;
    transform: translate(20px,20px);

}

</style>
