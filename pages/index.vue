<template>
<div id="home" class=" min-w-screen min-h-screen">

    <Header/>

    <main class="flex flex-col lg:flex-row justify-center lg:justify-around items-center mb-6 px-4 lg:px-16">
        <div class="text-green-400 w-full text-center lg:text-justify lg:w-3/6 font-light tracking-wide">
            <h3 class="text-xl"> 
                So, you want to travel to
            </h3>
            <span class="uppercase text-6xl font-bold lg:text-9xl my-5 inline-block">space</span><br>
            <p class="lg:w-2/4 text-lg lg:text-xl">
                Let’s face it; if you want to go to space, you might as well genuinely go to outer
                space and not hover kind of on the edge of it. Well sit back, and relax because
                we’ll give you a truly out of this world experience!
            </p>
        </div>
        <NuxtLink to="/destination" class="mt-10 lg:mt-28 lg:mr-10 uppercase rounded-full bg-white flex justify-center items-center w-52 h-52 text-4xl font-light text-slate-900">explore</NuxtLink>
    </main>

</div>
</template>

<script setup>
import data from '../data.json';
</script>

<style scoped>
#home {
    background: url('../assets/home/background-home-desktop.jpg');
    background-size: cover;
    overflow: hidden;
}

main {
    margin-top:100px;
}
@media (max-width: 850px){
    #home {
        background: url('../assets/home/background-home-tablet.jpg');
        background-size: cover;
    }
}
@media (max-width: 450px){
    #home {
        background: url('../assets/home/background-home-mobile.jpg');
        background-size: cover;
    }
}
</style>