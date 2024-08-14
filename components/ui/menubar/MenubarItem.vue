<script setup lang="ts">
import { type HTMLAttributes, computed } from 'vue'
import {
  MenubarItem,
  type MenubarItemEmits,
  type MenubarItemProps,
  useForwardPropsEmits,
} from 'radix-vue'
import { cn } from '@/lib/utils'

const props = defineProps<MenubarItemProps & { class?: HTMLAttributes['class'], inset?: boolean }>()

const emits = defineEmits<MenubarItemEmits>()

const delegatedProps = computed(() => {
  const { class: _, ...delegated } = props

  return delegated
})

const forwarded = useForwardPropsEmits(delegatedProps, emits)
</script>

<template>
  <MenubarItem
    v-bind="forwarded"
    :class="cn(
      'relative flex cursor-default select-none items-center rounded-sm p-[12px] text-sm outline-none focus:bg-[#FCF7F4] focus:text-[#E1AF93] data-[disabled]:pointer-events-none data-[disabled]:opacity-50',
      inset && 'pl-8',
      props.class,
    )"
  >
    <slot />
  </MenubarItem>
</template>
