<template>
    <div id="home" class=" min-w-screen min-h-screen">
        <Header/>
        
        <div>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Debitis, minima sapiente, unde perferendis sed dolor natus expedita iure quam autem eligendi repudiandae rerum dicta quas hic omnis aut corrupti cupiditate beatae? Nisi, ipsum. Sed quis mollitia possimus eos facere omnis ullam, odit sint harum laboriosam, ea commodi repellendus accusantium quos.x
        </div>
        
    </div>
</template>

<script setup>

</script>

<style scoped>
#home {
    background: url('../assets/technology/background-technology-desktop.jpg');
    background-size: cover;
    overflow: hidden;
}
@media (max-width: 850px){
    #home {
        background: url('../assets/technology/background-technology-tablet.jpg');
        background-size: cover;
    }
}
@media (max-width: 450px){
    #home {
        background: url('../assets/technology/background-technology-mobile.jpg');
        background-size: cover;
    }
}
</style>