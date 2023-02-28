<script setup lang="ts">
    function moveToAbout() {
        navigateTo("about");
    }
</script>

<template>
    <div>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="about">About</NuxtLink>
        <button @click="moveToAbout">Take me to about</button>
    </div>
    <div>
        Hi there
    </div>
    
</template>