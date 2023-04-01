<template>
    <div id="home" class=" min-w-screen min-h-screen">
        <Header/>
        
        <Crew/>
        
    </div>
</template>

<script setup>

</script>

<style scoped>
#home {
    background: url('../assets/crew/background-crew-desktop.jpg');
    background-size: cover;
    overflow: hidden;
}
@media (max-width: 850px){
    #home {
        background: url('../assets/crew/background-crew-tablet.jpg');
        background-size: cover;
    }
}
@media (max-width: 450px){
    #home {
        background: url('../assets/crew/background-crew-mobile.jpg');
        background-size: cover;
    }
}
</style>