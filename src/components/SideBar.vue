<script setup>
import { ref } from 'vue'
const sideBarToggle = ref(true)
const sideBar = ref([
    {
        icon: 'src/assets/imgs/sideBarImgs/დეშბორდი (1).png',
        class: 'text-white ms-3',
        title: 'დეშბორდი'
    },
    {
        icon: 'src/assets/imgs/sideBarImgs/განცხადებები.png',
        class: 'text-white ms-3',
        title: 'განცხადებები'
    },
    {
        icon: 'src/assets/imgs/sideBarImgs/შეტყობინებები.png',
        class: 'text-white ms-3',
        title: 'შეტყობინებები'
    },
    {
        icon: 'src/assets/imgs/sideBarImgs/კურსები.png',
        class: 'text-white ms-3',
        title: 'ჩემი კურსები'
    },
    {
        icon: 'src/assets/imgs/sideBarImgs/Vector.png',
        class: 'text-white ms-3',
        title: 'ლიდერბორდი'
    },
    {
        icon: 'src/assets/imgs/sideBarImgs/profile_round-[#1342].png',
        class: 'text-white ms-3 ',
        title: 'ჩემი პროფილი'
    },
    {
        icon: 'src/assets/imgs/sideBarImgs/Vector (1).png',
        class: 'text-[#FF0000] ms-3 ',
        title: 'გასვლა'
    },
])
</script>

<template>

    <aside v-show="sideBarToggle" class=" w-96 h-screen transition-transform -translate-x-full sm:translate-x-0"
        aria-label="Sidebar">
        <div class="h-full px-3 py-4 overflow-y-auto bg-[#1B2532] ">

            <a href="" class="flex items-center ps-2.5 mb-5">
                <img src="https://flowbite.com/docs/images/logo.svg" class="h-6 me-3 sm:h-7" alt="Flowbite Logo" />
                <span class="self-center text-xl font-semibold whitespace-nowrap text-white ">Flowbite</span>
            </a>
            <ul v-for="item in sideBar" :key="item.index" class="space-y-2 ">
                <li>
                    <a href="#" class="flex items-center p-4 text-xl rounded-lg font-light  hover:bg-gray-700 ">
                        <img class="w-4 h-4 mt-1.5" :src="item.icon" alt="">
                        <span :class="item.class">{{ item.title }}</span>
                    </a>
                </li>
            </ul>
            <!-- <div class='flex gap-x-3 '>
        <img class="w-4 h-4 mt-1.5" src="/src/assets/imgs/sideBarImgs/Vector (3).png" alt="">
        <div class="text-white">დახმარება</div>
      </div> -->
        </div>
    </aside>
    <button @click="sideBarToggle = !sideBarToggle" class="inline text-white bg-[#0A0C11] flex justify-start "> <svg
            xmlns="http://www.w3.org/2000/svg" width="44" height="44" fill="currentColor" class="bi bi-justify "
            viewBox="0 0 16 16">
            <path fill-rule="evenodd"
                d="M2 12.5a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5m0-3a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5m0-3a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5m0-3a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5" />
        </svg>
    </button>
</template>