<script setup>
import { ref } from 'vue'

const data = ['tema 1','tema 2','tema 3','tema 4']

const selectedIndex = ref(0)

function showInfo(i){
  if(i == selectedIndex.value){
    selectedIndex.value = -1
  }else {
    selectedIndex.value = i
  }
}
</script>
<template>
  <div 
    class="bg-blue-500 p-2 max-w-[400px] mx-auto mt-12 rounded"
  >
    <div class="mb-2 " 
      v-for="(theme, i) in data"
      :key="i"
    >
      <h1
        @click="showInfo(i)"
        class="bg-blue-400 text-white px-1 flex justify-between hover:cursor-pointer select-none h-8 rounded"
        :class="{'bg-blue-600': selectedIndex == i}"
       >
        {{ theme }}
        <span>{{ selectedIndex == i ? '-': '+' }}</span>
      </h1>
      <div 
        v-show="selectedIndex == i"
        class="bg-blue-50/50 p-1 mt-1 h-24"
        >
        Texto tema 1
      </div>
    </div> 
  </div>
</template>