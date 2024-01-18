<script setup>
import { ref } from 'vue'
import SideBar from '../components/SideBar.vue'
import NavBar from '../components/NavBar.vue'
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'
import { Pie } from 'vue-chartjs'
import { data, options } from '../chartConfig.ts'

ChartJS.register(ArcElement, Tooltip, Legend)

const components = defineProps(['Pie'])
const chartData = ref(data)
const chartOptions = ref(options)


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
      <div class="flex flex-col gap-y-32">
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

      <div class="w-96 ml-36 ">
        <div class=" bg-[#1B2532] rounded-3xl py-6">
          <h3 class="text-white text-2xl px-16 pb-6">ტოპ მასწავლებლები</h3>
          <div class=" ">
            <Pie class="w-64" :data="chartData" :options="chartOptions" />
          </div>
        </div>
      </div>
      </div>
      




    </div>
  </div>
</template>