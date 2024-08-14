<script  setup>
const openDropdown = ref(false)
</script>
<template>
    <ul class="flex items-center gap-[50px]">
       <li class="cursor-pointer">
           <option to="">Услуги</option>
       </li> 
       <li class="cursor-pointer">
           <NuxtLink to="/about">О нас</NuxtLink>
       </li> 
       <li class="cursor-pointer">
           <NuxtLink to="/blog">Блог</NuxtLink>
       </li> 
       <li class="cursor-pointer">
           <NuxtLink to="/contacts">Контакты</NuxtLink>
       </li> 
    </ul>
</template>
