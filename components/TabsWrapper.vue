<script setup>
import { useSlots, ref , provide} from 'vue'
import data from '../data.json' 
const slots = useSlots()
const tabTitles = ref(slots.default().map(tab => tab.props.title))
const selectedTitle = ref(tabTitles.value[0])

provide('selectedTitle', selectedTitle)

</script>

<template>
    <div class="tabs lg:m-0">
        <ul class="tabs__header">

            <li 
                v-for="title in tabTitles" 
                :key="title"
                class="tabs__item capitalize"
                :class="{ selected: selectedTitle === title}"
                @click="selectedTitle = title"
            >
                {{ title }}
            </li>

        </ul>

        <slot />
    </div>
</template>

<style>


.tabs__header {
    list-style: none;
    max-width: 80vw;
    padding: 0;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    gap: 5px;
}

.tabs__item {
    /* flex: 1; */
    cursor: pointer;
    user-select: none;
    /* transition: 0.3s; */

}
.tabs__item:hover {
    border-bottom: 2px solid #555;
}
.tabs__item.selected {
    /* background-color: #5f567a; */
    border-bottom: 2px solid #ccc;
}

.tabs__content {
    /* background-color: #bfbfbf; */
    min-height: 300px;
    display: grid;
    place-items: center;
    border-radius: 0 0 5px 5px;
    padding: 10px;
}

@media (min-width: 1024px){
    .tabs{
        /* max-width: 70vw; */
        widows: 50%;
        max-height: 50%;
        margin: 0 ;
        padding: 0;
    }
    .tabs__header{
        width: 70%;
    }
}
</style>