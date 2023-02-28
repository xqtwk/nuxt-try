<script setup lang="ts">
  /*//const MyComponent = shallowRef(resolveComponent("Counter"));
  const MyComponent = ref("Counter");
  function toggle() {
    //MyComponent.value = resolveComponent("Hello");
    MyComponent.value = "Hello";
  }*/
  const page = ref("");
  function view(name:string) {
    page.value = name;
  }

</script>
<template>
  <div>
    <h3>Hello, World!</h3>
  </div>
  <div>
  <!-- <button @click="toggle">Toggle</button> -->
  </div>
  <a href="#" @click="view('Hello')">Hello</a>
  <br/>
  <a href="#" @click="view('Counter')">Counter</a>

  <NuxtPage/> <!-- Depends on what page you're visiting. URL/ will render index at this point of the page,
  URL/about will render about. -->

  <!-- If don't want to use App.vue - just rename it to anything else, like aoigfdag.vue and nuxt will stop using it as "doorway"-->

    <Hello v-if="page == 'Hello'" />
  <LazyCounter v-if="page == 'Counter'" />  <!-- LAZY COMPONENT ONLY IMPORTED WHEN NEEDED-->
  <!-- <component :is="MyComponent" /> -->
  <!-- <Counter /> -->
</template>
