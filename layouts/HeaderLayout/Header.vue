<script setup>
import HeaderMenu from './components/HeaderMenu.vue'
import HeaderButtons from './components/HeaderButtons.vue'
</script>
<template>
    <header>
        <div class="container flex justify-between items-center p-[20px]">
            <div class="logo">
                <img src="../../assets/images/logo.svg" alt="">
            </div>
            <HeaderMenu/>
            <HeaderButtons/>
        </div>
    </header>
</template>