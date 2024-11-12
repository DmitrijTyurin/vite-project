<template>
    <div class="composition">
        <div>
            <h2>Первая домашка</h2>
            <p>Counter: {{ count }}</p>
            <button @click="increment">+</button>
        </div>
        <div>
            <button @click="toggle">Жмяк</button>
            <p v-if="isVisible">Первые знакомства с Vue.JS.</p>
        </div>
    </div>
</template>

<script setup>
  import {ref} from 'vue'
  
  const count = ref(0)
  const increment = () => {
    count.value++
  }

  const isVisible = ref(false)
  const toggle = () => {
    isVisible.value = !isVisible.value
  }
</script>

<style lang="scss" scoped>
  .composition {
    width: 400px;
  }
</style>