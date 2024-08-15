<script setup>
import {
    Pagination,
    PaginationEllipsis,
    PaginationFirst,
    PaginationLast,
    PaginationList,
    PaginationListItem,
    PaginationNext,
    PaginationPrev,
} from '@/components/ui/pagination'
import {
    Select,
    SelectContent,
    SelectGroup,
    SelectItem,
    SelectLabel,
    SelectTrigger,
    SelectValue,
} from '@/components/ui/select'
</script>
<template>
    <div class="flex  justify-between">
        <div class="flex items-center gap-[20px]">
            <p class="text-[#858585] text-[18px]">Показывать на странице: </p>
            <Select class="ml-[10px]">
                <SelectTrigger>
                    <SelectValue placeholder="10" value="10" />
                </SelectTrigger>
                <SelectContent>
                    <SelectGroup>
                        <SelectItem value="10">
                            10
                        </SelectItem>
                        <SelectItem value="20">
                            20
                        </SelectItem>
                        <SelectItem value="30">
                            30
                        </SelectItem>
                    </SelectGroup>
                </SelectContent>
            </Select>
        </div>
        <Pagination v-slot="{ page }" :total="100" :sibling-count="1" show-edges :default-page="2">
            <PaginationList v-slot="{ items }" class="flex items-center gap-1">
                <PaginationFirst />
                <PaginationPrev />

                <template v-for="(item, index) in items">
                    <PaginationListItem v-if="item.type === 'page'" :key="index" :value="item.value" as-child>
                        <Button class="w-10 h-10 p-0 " :class="item.value === page ? 'bg-[#E1AF93]' : ''" :variant="item.value === page ? 'default' : 'outline'">
                            {{ item.value }}
                        </Button>
                    </PaginationListItem>
                    <PaginationEllipsis v-else :key="item.type" :index="index" />
                </template>

                <PaginationNext />
                <PaginationLast />
            </PaginationList>
        </Pagination>
    </div>
</template>