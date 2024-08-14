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
</script>
<template>
    <section class="states-section">
        <div class="container">
            <TitleUi>Статьи</TitleUi>

            <Tabs default-value="all" class="w-[400px] mt-[40px]">
                <TabsList class="">
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
                    Make changes to your account here.
                </TabsContent>
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