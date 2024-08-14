<script setup lang="ts">
import { type HTMLAttributes, computed } from 'vue'
import { TabsTrigger, type TabsTriggerProps, useForwardProps } from 'radix-vue'
import { cn } from '@/lib/utils'

const props = defineProps<TabsTriggerProps & { class?: HTMLAttributes['class'] }>()

const delegatedProps = computed(() => {
  const { class: _, ...delegated } = props

  return delegated
})

const forwardedProps = useForwardProps(delegatedProps)
</script>

<template>
  <TabsTrigger
    v-bind="forwardedProps"
    :class="cn(
      'inline-flex text-black  items-center justify-center whitespace-nowrap  px-[30px] py-[12px] text-sm font-medium bor ring-offset-background transition-all focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 data-[state=active]:bg-[#E1AF93] data-[state=active]:text-[#ffffff] data-[state=active]:shadow-sm',
      props.class,
    )"
  >
    <slot />
  </TabsTrigger>
</template>
<style scoped>
.bor{
  border: 1px solid #EAEAEA;
}
</style>