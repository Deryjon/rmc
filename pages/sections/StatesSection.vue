<script setup lang="ts">
import {
    Menubar,
    MenubarCheckboxItem,
    MenubarContent,
    MenubarItem,
    MenubarMenu,
    MenubarRadioGroup,
    MenubarRadioItem,
    MenubarSeparator,
    MenubarShortcut,
    MenubarSub,
    MenubarSubContent,
    MenubarSubTrigger,
    MenubarTrigger,
} from '@/components/ui/menubar'
import TitleUi from '@/components/TitleUI.vue'
const data = [
    {
        img: 'home-4.jpg',
        date: '31.07.2024',
        views: 899,
        title: 'Тенденции и прогнозы рынка недвижимости на 2024 год'
    },
    {
        img: 'home-5.jpg',
        date: '31.07.2024',
        views: 899,
        title: 'Лучшие районы для инвестиций в недвижимость'
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
    <section class="states-section">
        <div class="container">
            <TitleUi>Статьи</TitleUi>

            <Tabs default-value="all" class="w-[400px] mt-[40px]">
                <TabsList>
                    <TabsTrigger value="all">
                        Все
                    </TabsTrigger>
                    <TabsTrigger value="apartment">
                        О недвижимости
                    </TabsTrigger>
                    <TabsTrigger value="investor">
                        Инвесторам
                    </TabsTrigger>
                    <TabsTrigger value="buy-apartment">
                        Покупка недвижимости
                    </TabsTrigger>
                    <TabsTrigger value="district">
                        Обзоры районов
                    </TabsTrigger>
                    <Menubar>
                        <MenubarMenu>
                            <MenubarTrigger class="flex items-center gap-[10px]">Сортировать
                                <Icon name="fluent:arrow-sort-16-filled" size="22" />
                            </MenubarTrigger>
                            <MenubarContent>
                                <MenubarItem>
                                    По дате: сначала новые
                                </MenubarItem>
                                <MenubarItem>
                                    По дате: сначала старые
                                </MenubarItem>
                                <MenubarItem>
                                    По популярности
                                </MenubarItem>
                            </MenubarContent>
                        </MenubarMenu>
                    </Menubar>
                </TabsList>

                <TabsContent value="all">
                    <div class="flex gap-[30px] mt-[30px]">
                        <div class="card">
                            <div class="top text-[20px] relative w-[430px] h-[290px]">
                                <img src="../../assets/images/home-4.jpg" alt="" class="w-full h-full">
                                <div class="flex justify-between absolute w-full text-white bottom-[-5px] p-[20px]">
                                    <p>{{ data[0].date }}</p>
                                    <p class="flex items-center gap-[2.5px]">
                                        <Icon name="ph:eye" size="24" />
                                        {{ data[0].views }}
                                    </p>
                                </div>
                            </div>
                            <div class="texts mt-[20px]">
                                <p class="text-[24px]">{{ data[0].title }}</p>
                                <p class="text-[18px] mt-[20px] text-[#E1AF93] flex gap-[4px] items-center">
                                    Подробнее
                                    <Icon name="mingcute:arrow-right-fill" size="20" color="#E1AF93" />
                                </p>
                            </div>
                        </div>
                        <div class="card">
                            <div class="top text-[20px] relative w-[430px] h-[290px]">
                                <img src="../../assets/images/home-5.jpg" alt="" class="w-full h-full">

                                <div class="flex justify-between absolute w-full text-white bottom-[-5px] p-[20px]">
                                    <p>{{ data[1].date }}</p>
                                    <p class="flex items-center gap-[2.5px]">
                                        <Icon name="ph:eye" size="24" />
                                        {{ data[1].views }}
                                    </p>
                                </div>
                            </div>
                            <div class="texts mt-[20px]">
                                <p class="text-[24px]">{{ data[1].title }}</p>
                                <p class="text-[18px] mt-[20px] text-[#E1AF93] flex gap-[4px] items-center">
                                    Подробнее
                                    <Icon name="mingcute:arrow-right-fill" size="20" color="#E1AF93" />
                                </p>
                            </div>
                        </div>
                        <div class="card">
                            <div class="top text-[20px] relative w-[430px] h-[290px]">
                                <img src="../../assets/images/home-6.jpg" alt="" class="w-full h-full">

                                <div class="flex justify-between absolute w-full text-white bottom-[-5px] p-[20px]">
                                    <p>{{ data[2].date }}</p>
                                    <p class="flex items-center gap-[2.5px]">
                                        <Icon name="ph:eye" size="24" />
                                        {{ data[2].views }}
                                    </p>
                                </div>
                            </div>
                            <div class="texts mt-[20px]">
                                <p class="text-[24px]">{{ data[2].title }}</p>
                                <p class="text-[18px] mt-[20px] text-[#E1AF93] flex gap-[4px] items-center">
                                    Подробнее
                                    <Icon name="mingcute:arrow-right-fill" size="20" color="#E1AF93" />
                                </p>
                            </div>
                        </div>

                    </div>
                </TabsContent>

                <!-- Остальные вкладки -->
                <TabsContent value="apartment">
                    Change your password here.
                </TabsContent>
                <TabsContent value="investor">
                    Change your password here.
                </TabsContent>
                <TabsContent value="buy-apartment">
                    Change your password here.
                </TabsContent>
                <TabsContent value="district">
                    Change your password here.
                </TabsContent>
            </Tabs>

        </div>
    </section>
</template>
