<template>
  <div class="social">
        <svg id="facebook" data-name="facebook" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 145.83 50">
            <title>facebook</title>
            <line id="ligne" class="cls-3" x1="48.17" y1="25.02" x2="-1.5" y2="25.02"/>
            <path class="cls-3" d="M100.18,28.55l-.09,16a2.14,2.14,0,0,0,2.12,2.13h4a2,2,0,0,0,2-2V28.37a1.06,1.06,0,0,1,1.05-1.06h5.39a1,1,0,0,0,1-.85l1.21-6.07a1,1,0,0,0-.82-1.24l-.18,0h-6.61a1,1,0,0,1-1-1V13.69s-.44-2.75,3.81-2.75h3A1.93,1.93,0,0,0,117,9V3.72a.87.87,0,0,0-.86-.86h-6.65c-1.9,0-9.63,0-9.73,15.23a1.05,1.05,0,0,1-1.05,1.07h-4.6a1.05,1.05,0,0,0-1.06,1.06l.1,6.19a1.06,1.06,0,0,0,1,1.06h5A1.07,1.07,0,0,1,100.18,28.55Z"/>
        </svg>
    
    <a href="">
        <svg id="linkedin" data-name="linkedin" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 180 50">
            <title>linkedin</title>
            <line id="ligne" class="cls-3" x1="48.17" y1="25.02" x2="-1.5" y2="25.02"/>
            <ellipse class="cls-3" cx="94.72" cy="8.76" rx="5.55" ry="5.11"/>
            <rect class="cls-3" x="90.84" y="16.76" width="8.52" height="28.34" rx="2.07" ry="2.07"/>
            <path class="cls-3" d="M104.92,43.55V18.92a1.43,1.43,0,0,1,1.43-1.45h.12l6.19.51a1.51,1.51,0,0,1,1.16.77l.31.59a1.45,1.45,0,0,0,2,.61l0,0a1.67,1.67,0,0,0,.28-.18c2.61-2.33,8.8-6.34,15-.34a8.47,8.47,0,0,1,2.36,4.32c.6,2.76,1.24,8,1.16,20a1.45,1.45,0,0,1-1.42,1.45h-7.23a1.45,1.45,0,0,1-1.43-1.45l0-12.87a4.24,4.24,0,0,0-4.35-4.13h0a3.69,3.69,0,0,0-.47,0c-4.36.24-5,3.7-5,4.23v.14l-.36,12.54a1.48,1.48,0,0,1-1.47,1.42L106.33,45A1.46,1.46,0,0,1,104.92,43.55Z"/>
        </svg>
    </a>
    
    <a href="">
        <svg id="instagram" data-name="instagram" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 156.33 50">
            <title>instagram</title>
            <path id="carre" class="cls-3" d="M104.53,3.48A12.74,12.74,0,0,0,91.81,16.2V33.8a12.74,12.74,0,0,0,12.72,12.72h17.6A12.74,12.74,0,0,0,134.85,33.8V16.2A12.74,12.74,0,0,0,122.13,3.48Zm8.8,10.76A10.76,10.76,0,1,1,102.57,25a10.76,10.76,0,0,1,10.76-10.76Z"/>
            <circle id="rond1" class="cls-2" cx="127.02" cy="12.45" r="2.19"/>
            <line id="ligne" class="cls-3" x1="48.17" y1="25.02" x2="-1.5" y2="25.02"/>
        </svg>
    </a>
            
  </div>
</template>

<script>
export default {
  name: 'Social'
}
</script>

<style scoped>
.cls-3{fill:none;stroke:#FAFAFA;stroke-miterlimit:10;stroke-width:2px;}
.cls-2{fill:none;stroke-miterlimit:10;stroke:#FAFAFA;}

#facebook, #instagram, #linkedin{
    height: 25px;
}

.social *{
    transition: 0.3s;
}

#facebook:hover #ligne{
    animation-duration: 0.3s;
    transform: translateX(-100px);

}

#facebook:hover .cls-3{
    animation-duration: 0.3s;
    fill: #FAFAFA;
    stroke-width: 1px;
    transform: translateX(20px);
}


#linkedin:hover #ligne{
    animation-duration: 0.3s;
    transform: translateX(-100px);

}

#linkedin:hover .cls-3{
    animation-duration: 0.3s;
    fill: #FAFAFA;
    stroke-width: 1px;
    transform: translateX(20px);
}

#instagram:hover #ligne{
    animation-duration: 0.3s;
    transform: translateX(-100px);

}

#instagram:hover .cls-3{
    animation-duration: 0.3s;
    fill: #FAFAFA;
    stroke-width: 1px;
    transform: translateX(20px);
}

#instagram:hover .cls-2{
    animation-duration: 0.3s;
    transform: translateX(20px); 
    fill: DarkSlateBlue;
}

</style>