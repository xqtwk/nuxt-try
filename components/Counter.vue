<script setup lang="ts">
  const count = ref(0);
  function increment() {
    count.value++;
  }
  function decrement() {
    count.value--;
  }
</script>
<template>
    <div>
        <button @click="increment">Increment</button>
        <p>{{ count }}</p>
        <button @click="decrement">Decrement</button>
    </div>

</template>