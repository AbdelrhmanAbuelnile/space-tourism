<template>

    <div class="w-full h-screen bg-[#0f1025]" v-if="show">
        <div class="flex flex-row justify-between items-center p-5">
            <img src="../assets/shared/logo.svg" alt="logo" class="m-0">
            <img src="../assets/shared/icon-close.svg" alt="close" class="m-0" @click="showMe">
        </div>
        <ul class="">
            <li><NuxtLink to="/"            class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4 mx-5 my-8"><span class="font-bold tracking-normal">00</span>home</NuxtLink></li>
            <li><NuxtLink to="/destination" class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4 mx-5 my-8"><span class="font-bold tracking-normal">01</span>destinations</NuxtLink></li>
            <li><NuxtLink to="/crew"        class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4 mx-5 my-8"><span class="font-bold tracking-normal">02</span>crew</NuxtLink></li>
            <li><NuxtLink to="/technology"  class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4 mx-5 my-8"><span class="font-bold tracking-normal">03</span>technology</NuxtLink></li>
        </ul>
    
    </div>

    <div id="max" class="flex flex-row justify-between lg:items-center items-start lg:px-16 p-4 lg:py-9 w-full" >
        <img src="../assets/shared/logo.svg" alt="logo">
        <div class="w-2/6 border-b-2 border-gray-800 mn"></div>
        <ul class="nav">
            <li><NuxtLink to="/" class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">00</span>home</NuxtLink></li>
            <li><NuxtLink to="/destination" class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">01</span>destinations</NuxtLink></li>
            <li><NuxtLink to="/crew" class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">02</span>crew</NuxtLink></li>
            <li><NuxtLink to="/technology" class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">03</span>technology</NuxtLink></li>
        </ul>

        <img src="../assets/shared/icon-hamburger.svg" @click="showMe" id="nov" alt="menu logo" class="lg:hidden mt-3">
    </div>


    <div id="manga">
        <ul class="flex flex-col gap-10 justify-center items-start mt-20 p-10 w-full">
            <li><NuxtLink to="/"             class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">00</span>home</NuxtLink></li>
            <li><NuxtLink to="/destination"  class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">01</span>destinations</NuxtLink></li>
            <li><NuxtLink to="/crew"         class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">02</span>crew</NuxtLink></li>
            <li><NuxtLink to="/technology"   class="text-gray-200 text-lg font-light uppercase tracking-[5px] flex gap-4"><span class="font-bold tracking-normal">03</span>technology</NuxtLink></li>
        </ul>
    </div>

</template>

<script setup>
import { ref, onMounted } from 'vue'

// const change = ()=>{
//     const manga = document.getElementById('manga')
//     const max = document.getElementById('max')
//     const nov = document.getElementById('nov')
//     max.style.background = "#0f1025"
//     max.style.height = '100%'
//     max.style.position = 'absolute'
//     manga.style.display = "block"
//     manga.style.width = "100%"
//     manga.style.height = "100%"
//     // nov.src = "../assets/shared/icon-close.svg"

// }


let show = false
const showMe = ()=>{
    show = !show
    console.log(show)
}


</script>

<style scoped>

#manga {
    display: none;
    z-index: 999;
    position: absolute;

}
.router-link-exact-active {
        border-bottom:#ccc solid 1px ;
}
@media (max-width:950px){
    .nav, .mn {
        display: none;
    }
}
</style>