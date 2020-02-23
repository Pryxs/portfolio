<template>
    <div id="navigation">
        <div id="laptopNav" v-if="this.$store.state.isMobile == false">
            <router-link to="/projets">
                <svg id="cercle" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 60 60">
                        <title>navigation</title>
                        <path id="droit" class="cls-1" d="M27,1a15,15,0,0,1,0,30"/>
                        <path id="gauche" class="cls-1" d="M27,31A15,15,0,0,1,27,1"/>
                        <line id="ligne" class="cls-1" x1="27" y1="31" x2="27" y2="70"/>        
                    </svg>
                    <label id="proj">Projets</label>
            </router-link>
            <router-link to="/about">
            <svg id="cercle" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 60 60">
                        <title>navigation</title>
                        <path id="droit" class="cls-1" d="M27,1a15,15,0,0,1,0,30"/>
                        <path id="gauche" class="cls-1" d="M27,31A15,15,0,0,1,27,1"/>
                        <line id="ligne" class="cls-1" x1="27" y1="31" x2="27" y2="70"/>        
                    </svg>
                    <label id="propos">A propos</label>
            </router-link>
        </div>

        <div id="mobileNav" v-if="this.$store.state.isMobile == true">
            <nav>
                <router-link to="/projets">
                    <label>Projets</label>
            </router-link>

            <router-link to="/about">
                    <label>A propos</label>
            </router-link>                
            </nav>
        </div>
    </div>

    
</template>

<script>
export default {
  name: 'Navigation'
}
</script>

<style scoped>
.cls-1{fill:none;stroke:#FAFAFA;stroke-miterlimit:10;stroke-width:1px;}


#laptopNav{
   position: absolute;
    top: 100%;
    transform: translateY(-90%);
    display: flex;
    left: calc(50% - 300px);
}


#proj, #propos{
    position: relative;
    left: -50%;
    top: -65%;
    opacity: 0;  
    text-decoration: none;
    color: #FAFAFA;
    font-family: Questrial, sans-serif;
    font-size: 20px;
} 

#laptopNav a{
    height: 80px;
    min-width: 250px;
    text-decoration: none;
}

#cercle {
    height: 80px;
    width: 250px;
    animation-duration: 2s;
    animation-fill-mode: forwards;
}

a:hover #ligne{
    transition: 0.3s;
    transform: translateY(40px);
}

a *{
   transition: 0.3s;
}

a:hover #droit{
    animation-duration: 0.3s;
    transform: translateX(50px);

}

a:hover #gauche{
    animation-duration: 0.3s;
    transform: translateX(-50px);
}

a:hover #proj{
    animation-duration: 0.3s;
    opacity: 1;
}  



a:hover #ligne{
    animation-duration: 0.3s;
    transform: translateY(40px);
}

a:hover #droit{
    animation-duration: 0.3s;
    transform: translateX(50px);
}

a:hover #gauche{
    animation-duration: 0.3s;
    transform: translateX(-50px);
}

a:hover #propos{
    animation-duration: 0.3s;
    opacity: 1; 
}

#mobileNav{
     position: absolute;
    top: 100%;
    transform: translateY(-90%);
    width: 100%;
}

nav{
    display: flex;
    justify-content: space-around;    
}

#mobileNav a{
    color: white;
    font-size: 25px;
    margin-bottom: 20px;
    text-decoration: none;
}

</style>