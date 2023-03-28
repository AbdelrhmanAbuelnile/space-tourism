<template>
    <div id="home" class=" min-w-screen min-h-screen">
        <Header/>
        
        <div class="flex flex-col justify-center items-center mx-auto gap-5 lg:items-start lg:felx-row lg:px-10 lg:justify-between">
            <h2 class="text-center text-2xl tracking-widest text-white"><span class="text-gray-600">01</span> Pick your destination</h2>
            <div class="lg:flex lg:flex-row lg:items-center lg:justify-between">
                <img src="../assets/destination/image-moon.png" class="w-3/4 lg:w-2/5 lg:mx-0 mx-auto my-10" alt="destination image">
                <div class="text-white text-lg lg:w-2/5 lg:mx-0">
                    <TabsWrapper class="w-5/5 lg:mx-0 text-center ">
                        <TabItem title="moon">
                            <div class="bor text-gray-500">
                                {{ data.destinations[0].description }}
                            </div>
                            <div class="mt-5">
                                <div class="text-white text-3xl mb-5">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">avg. distance</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[1].distance}}</p>
                                </div> 
                                <div class="text-white text-3xl">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">est. travel time</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[1].travel}}</p> 
                                </div>
                            </div>
                        </TabItem>
                        <TabItem title="mars">
                            <div class="bor text-gray-500">
                                {{ data.destinations[1].description }}
                            </div>
                            <div class="mt-5">
                                <div class="text-white text-3xl mb-5">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">avg. distance</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[2].distance}}</p>
                                </div> 
                                <div class="text-white text-3xl">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">est. travel time</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[2].travel}}</p> 
                                </div>
                            </div>
                        </TabItem>
                        <TabItem title="europa">
                            <div class="bor text-gray-500">
                                {{ data.destinations[2].description }}
                            </div>
                            <div class="mt-5">
                                <div class="text-white text-3xl mb-5">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">avg. distance</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[3].distance}}</p>
                                </div> 
                                <div class="text-white text-3xl">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">est. travel time</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[3].travel}}</p> 
                                </div>
                            </div>
                        </TabItem>
                        <TabItem title="titan">
                            <div class="bor text-gray-500">
                                {{ data.destinations[3].description }}
                            </div>
                            <div class="mt-5">
                                <div class="text-white text-3xl mb-5">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">avg. distance</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[0].distance}}</p>
                                </div> 
                                <div class="text-white text-3xl">
                                    <h1 class="uppercase text-gray-500 font-light text-lg tracking-widest mb-3">est. travel time</h1>
                                    <p class="font-light uppercase tracking-widest">{{data.destinations[0].travel}}</p> 
                                </div>
                            </div>
                        </TabItem>

                        
                    </TabsWrapper>
                </div>
            </div>
        </div>
        
    </div>
</template>

<script setup>
import data from '../data.json' 

</script>

<style scoped>
#home {
    background: url('../assets/destination/background-destination-desktop.jpg');
    background-size: cover;
    overflow: hidden;
}
.bor {
    border-bottom: 1px solid #ccc;
    padding-bottom: 10px;
    width: 100%;
}
@media (max-width: 850px){
    #home {
        background: url('../assets/destination/background-destination-tablet.jpg');
        background-size: cover;
    }
}
@media (max-width: 450px){
    #home {
        background: url('../assets/destination/background-destination-mobile.jpg');
        background-size: cover;
    }
}
</style>