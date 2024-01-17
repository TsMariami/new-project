<script setup>
import { ref } from 'vue'
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
        <aside class=" w-96 h-screen transition-transform -translate-x-full sm:translate-x-0"
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
</template>