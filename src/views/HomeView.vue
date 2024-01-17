<script setup>
import { ref } from 'vue'
import SideBar from '../components/SideBar.vue'
import NavBar from '../components/NavBar.vue'

const myWrap = ref([
  {
    title: 'მეგობრები',
    number: '1256',
  },
  {
    title: 'განცხადებები',
    number: '18',
  },
  {
    title: 'კურსები',
    number: '3',
  },
  {
    title: 'დავალებები',
    number: '2',
  },
  {
    title: 'შეფასებები',
    number: '4.6/5.4',
  },
])
</script>
<template >
  <div class="flex">
    <SideBar />

    <div class="bg-[#0A0C11] w-full h-screen ">
      <NavBar />
      <div class="text-white ">
        <h3 class="text-4xl flex px-32 py-10 ">ჩემი შეფუთვა</h3>
        <div class="px-32 ">
          <div class=" bg-[#1B2532] rounded-3xl flex flex-row justify-between px-32    ">
            <div v-for="item in myWrap" :key="item.index"
              class=" flex text-center pt-6 pb-20 gap-y-12 text-white flex-col">
              <span class="text-xl">{{ item.title }}</span>
              <span class="text-3xl">{{ item.number }}</span>
            </div>
          </div>
        </div>
      </div>


      <div>
    <canvas id="myChart" ref="myChart"></canvas>
  </div>
    </div>
  </div>
</template>