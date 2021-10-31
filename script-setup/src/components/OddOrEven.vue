<template>
    <h1>D</h1>
    <p>{{ counter }}</p>
    <p>{{ result }}</p>
</template>



<script setup>
import {computed, watch} from "vue"


const props = defineProps({counter: Number})
const emit = defineEmits()
const result = computed(() => props.counter % 2 === 0 ? 'çift' : 'tek')

watch(result, (result) => {
    if(result === 'tek') emit("odd-event", true)
})

</script>