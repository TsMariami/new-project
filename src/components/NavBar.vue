<script setup>
import { ref } from 'vue'
const navBar = ref([
    {
        icon: 'src/assets/imgs/navBarImgs/Vector (4).png'
    },
    {
        icon: 'src/assets/imgs/navBarImgs/Vector (5).png'
    },
    {
        icon: 'src/assets/imgs/navBarImgs/image 1.png'
    },
])
</script>
<template>
    <div>
        <div class="flex justify-end ">
            <ul v-for="item in navBar" :key="item.index">
                <li class="p-4">
                    <img :src="item.icon" alt="">
                </li>
            </ul>
        </div>
    </div>
</template>