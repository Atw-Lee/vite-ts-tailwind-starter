<script setup lang="ts">
const store = useStore()
const count = computed(() => store.count)
defineProps<{
  msg: string
  optionalProp?: number
}>()

function increment() {
  store.increment()
}
</script>

<template>
  <h2>{{ msg }}</h2>
  <button @click="increment">
    <span class="h-7 pl-1">count is: {{ count }}</span>
  </button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
</template>
