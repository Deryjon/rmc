<script setup>

const data = [
    {
        img: 'home-4.jpg',
        date: '31.07.2024',
        views: 899,
        title: 'Преимущества покупки жилья на этапе строительства'
    },
    {
        img: 'home-5.jpg',
        date: '31.07.2024',
        views: 899,
        title: 'Современные технологии в строительстве: что ожидать от новостроек'
    },
    {
        img: 'home-6.jpg',
        date: '30.07.2024',
        views: 899,
        title: `Топ-10 новых \n 
        жилых комплексов для покупки`
    }

]
</script>
<template>
<div class="flex gap-[20px] justify-between mt-[30px]">
                        <div class="card">
                            <div class="top text-[20px] relative w-[665px] h-[290px]">
                                <img src="../../../assets/images/home-8.png" alt="" class="w-full h-full object-cover">
                                <div class="flex justify-between absolute w-full text-white bottom-[-5px] p-[20px]">
                                    <p>{{ data[0].date }}</p>
                                    <p class="flex items-center gap-[2.5px]">
                                        <Icon name="ph:eye" size="24" />
                                        {{ data[0].views }}
                                    </p>
                                </div>
                            </div>
                            <div class="texts mt-[20px]">
                                <p class="text-[24px]">Преимущества покупки жилья
                                    <br/>
                                    на этапе строительства</p>
                                <p class="text-[18px] mt-[20px] text-[#E1AF93] flex gap-[4px] items-center">
                                    Подробнее
                                    <Icon name="mingcute:arrow-right-fill" size="20" color="#E1AF93" />
                                </p>
                            </div>
                        </div>
                        <div class="card">
                            <div class="top text-[20px] relative w-[665px] h-[290px]">
                                <img src="../../../assets/images/home-7.png" alt="" class="w-full h-full object-cover">

                                <div class="flex justify-between absolute w-full text-white bottom-[-5px] p-[20px]">
                                    <p>{{ data[1].date }}</p>
                                    <p class="flex items-center gap-[2.5px]">
                                        <Icon name="ph:eye" size="24" />
                                        {{ data[1].views }}
                                    </p>
                                </div>
                            </div>
                            <div class="texts mt-[20px]">
                                <p class="text-[24px]">Современные технологии в строительстве:
                                    <br/>   
                                    что ожидать от новостроек</p>
                                <p class="text-[18px] mt-[20px] text-[#E1AF93] flex gap-[4px] items-center">
                                    Подробнее
                                    <Icon name="mingcute:arrow-right-fill" size="20" color="#E1AF93" />
                                </p>
                            </div>
                        </div>

                    </div>
</template>