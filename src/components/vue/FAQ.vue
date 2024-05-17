<script setup>
import { ref } from 'vue'

const showThemel = ref(true)
const showTheme2 = ref(false)
const showTheme3 = ref(false)
const showTheme4 = ref(false)

function showInfo(index){
  if(index == 1){
    showThemel.value = true
    showTheme2.value = false
    showTheme3.value = false
    showTheme4.value = false
  }
  if(index == 2){
    showThemel.value = false
    showTheme2.value = true
    showTheme3.value = false
    showTheme4.value = false
  }
  if(index == 3){
    showThemel.value = false
    showTheme2.value = false
    showTheme3.value = true
    showTheme4.value = false
  }
  if(index == 4){
    showThemel.value = false
    showTheme2.value = false
    showTheme3.value = false
    showTheme4.value = true
  }
}

</script>
<template>

  <div class="bg-blue-500 p-1 max-w-60 mx-auto mt-12">
    <div class="mb-2 rounded ">
      <h1 @click="showInfo(1)"
       class="bg-blue-400 text-white px-1 flex justify-between hover:cursor-pointer select-none"
       >
        Tema1
        <span>{{ showThemel ? '-': '+' }}</span>
      </h1>
      <div 
      v-show="showThemel"
      class="bg-blue-50/50 p-1 mt-1"
      >
      Texto tema 1
    </div>
    </div> 

    <div class="mb-2">
      <h1 @click="showInfo(2)"
       class="bg-blue-400 text-white px-1 flex justify-between hover:cursor-pointer select-none"
       >
       Tema2
        <span>{{ showTheme2 ? '-': '+' }}</span>
      </h1>
      <div 
      v-show="showTheme2"
      class="bg-blue-50/50 p-1 mt-1"
      >
      Texto tema 2
    </div>
    </div> 

    <div class="mb-2">
      <h1 @click="showInfo(3)"
       class="bg-blue-400 text-white px-1 flex justify-between hover:cursor-pointer select-none"
       >
       Tema3
        <span>{{ showTheme3 ? '-': '+' }}</span>
      </h1>
      <div 
      v-show="showTheme3"
      class="bg-blue-50/50 p-1 mt-1"
      >
      Texto tema 3
    </div>
    </div> 

    <div class="mb-2">
      <h1 @click="showInfo(4)"
       class="bg-blue-400 text-white px-1 flex justify-between hover:cursor-pointer select-none"
       >
       Tema4
        <span>{{ showTheme4 ? '-': '+' }}</span>
      </h1>
      <div 
      v-show="showTheme4"
      class="bg-blue-50/50 p-1 mt-1"
      >
      Texto tema 4
    </div>
    </div> 
  </div>
</template>