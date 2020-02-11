<template>
    <div class="logo">
        <router-link to="/">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="100 100 652.38 652.38">
                <title>logo</title>
                <g id="logo" data-name="logo"><polyline class="cls-5" points="372.24 478.38 341.14 440.78 384.68 440.78 415.78 478.38 372.24 478.38"/>
                <path class="cls-5" d="M322.14,177.1c24.88,0,93.3,12.44,93.3,93.3s-65.44,91-99.44,91H230l14-27.92s58.63-.09,72-.08c27,0,68.34-13.22,68.34-63,0-43.54-37.34-62-66.34-62-1,0-11.41-.18-11.41-.18Z"/></g>
                </svg>
        </router-link>
    </div>
</template>

<script>
    export default {
  name: 'Logo',
}
</script>

<style>
.cls-5{fill:black;stroke:black;stroke-width:1px;}

.logo{
    width: 120px;
    padding: 20px 0 0 20px;
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