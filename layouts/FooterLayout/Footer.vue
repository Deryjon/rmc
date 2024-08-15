<script setup>
import FooterSocialLinks from './components/FooterSocialLinks.vue'
import FooterLinks from './components/FooterLinks.vue'
import FooterCopyright from './components/FooterCopyright.vue'
</script>
<template>
    <footer class="bg-[#F7F7F7]">
        <div class="container py-[50px] ">
            <div class=" flex items-center justify-between">

                <div class="logo">
                    <img src="../../assets/images/logo.svg" alt="">
                </div>
                <FooterSocialLinks />
            </div>
            <div class="mt-[50px] w-full bord"></div>
            <FooterLinks class="mt-[50px]" />
            <div class="mt-[50px] w-full bord"></div>
<FooterCopyright class="mt-[50px]" />
        </div>
    </footer>
</template>
<style>
.bord {
    border: 1px solid #EAEAEA;
}
</style>