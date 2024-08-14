<script setup>
import TitleUi from '@/components/TitleUI.vue'
const data = [
    {
        date: '01.08.2024',
        views: 235,
        title: 'Современные жилые комплексы предлагают расширенные удобства для жителей'
    },
    {
        date: '31.07.2024',
        views: 899,
        title: 'Рынок новостроек демонстрирует стабильный рост'
    },
    {
        date: '30.07.2024',
        views: 500,
        title: 'Цены на квартиры в новостройках продолжают расти'
    }
]
</script>
<template>
    <section class="popular-status mt-[40px]">
        <div class="container">
            <TitleUi>Популярные статьи</TitleUi>
            <div class="cards mt-[30px] flex justify-between text-[#FFFFFF]">
                <div class="left w-[890px] h-[600px]  p-[30px] flex flex-col justify-between">
                    <div class="top flex justify-between text-[20px]">
                        <p class="date">{{ data[0].date }}</p>
                        <p class="views flex items-center gap-[7px]">
                            <Icon name="ph:eye" size="24" />
                            {{ data[0].views }}
                        </p>
                    </div>
                    <div class="bottom">
                        <h3 class="text text-[35px] font-medium">{{ data[0].title }}</h3>
                        <p class="flex items-center gap-[7px] mt-[10px] text-[18px] cursor-pointer">Подробнее
                            <Icon name="mingcute:arrow-right-fill" size="22" />

                        </p>
                    </div>
                </div>
                <div class="right flex justify-between flex-col">
                    <div class="top w-[467px] h-[290px] flex justify-between flex-col p-[20px]">
                        <div class="top-text flex justify-between text-[20px]">
                            <p class="date">{{ data[1].date }}</p>
                            <p class="views flex items-center gap-[7px]">
                                <Icon name="ph:eye" size="24" />
                                {{ data[1].views }}

                            </p>
                        </div>
                        <div class="">
                            <h3 class=" text-[25px] font-medium">{{ data[1].title }}</h3>
                            <p class="flex items-center gap-[7px] mt-[10px] text-[18px] cursor-pointer">Подробнее
                                <Icon name="mingcute:arrow-right-fill" size="22" />

                            </p>
                        </div>
                    </div>
                    <div class="bottom w-[467px] h-[290px] flex justify-between flex-col p-[20px]">
                        <div class=" flex justify-between text-[20px]">
                            <p class="date">{{ data[2].date }}</p>
                            <p class="date">30.07.2024</p>
                            <p class="views flex items-center gap-[7px]">
                                <Icon name="ph:eye" size="24" />
                                {{ data[2].views }}

                            </p>
                        </div>
                        <div class="">
                            <h3 class=" text-[25px] font-medium">{{ data[2].title }}</h3>
                            <p class="flex items-center gap-[7px] mt-[10px] text-[18px] cursor-pointer">Подробнее
                                <Icon name="mingcute:arrow-right-fill" size="22" />

                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped>
.left {
    background-image: url(../../assets/images/home-1.jpg);
    background-size: cover;
}

.right .top {
    background-image: url(../../assets/images/home-2.jpg);
    background-size: cover;
}

.right .bottom {
    background-image: url(../../assets/images/home-3.jpg);
    background-size: cover;
}
</style>
