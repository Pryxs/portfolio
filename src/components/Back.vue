<template>
    <div class="retour">
        <router-link to="/projets">
                <label>Projects</label>
                <svg id="fleche" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 92.5 38">
                    <line class="cls-1" x1="4.5" y1="17.5" x2="64.5" y2="17.5"/>
                    <polyline id="triangle" class="cls-2" points="68.5 2.5 87.94 17.93 68.44 33.44"/>
                </svg>
        </router-link>
    </div>
</template>

<script>
    export default {
  name: 'Back'
}
</script>

<style scoped>
.cls-1,.cls-2{fill:none;stroke:#000;stroke-linecap:round;}
.cls-1{stroke-miterlimit:10;}.cls-2{stroke-linejoin:round;fill-rule:evenodd;}

.retour{
    width: 80px;
    position: relative;
    display: block;
    margin: 100px auto 0 auto;
    padding-bottom: 100px;
    background-color: #fafafa;
}

#fleche *{
    transition: 1s ease-in-out;
    
}
#fleche{
    width: 64px;
    position: absolute;
    top: 40px;
    left: 8px;
}

.retour a{
    font-size: 20px;
    font-family: NotoSans, sans-serif;
    text-decoration: none;
    color: black;
    text-align: center;
    transition: 0.3s ease-in-out;

}

.retour:hover a{
    font-weight: 500;
    letter-spacing: 2px;
    animation: 0.3s;

}

#fleche .cls-1{
    stroke-dasharray: 45 80 ;  
    stroke-dashoffset: 0;

    -webkit-animation-iteration-count: infinite;
-moz-animation-iteration-count: infinite;
-ms-animation-iteration-count: infinite;
-o-animation-iteration-count: infinite;
animation-iteration-count: infinite;
animation-name: test;             
animation-direction: normal;
animation-duration: 1s;
}

@keyframes test{
    to{
        stroke-dashoffset: 0;


    }

    from{
        stroke-dashoffset: 100;


    }
}


</style>
