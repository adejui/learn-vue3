<template>
    <div>
        <Counter name="Ade" initial-count="100" />
        <Counter name="Jui" initial-count="100" />

        <CounterStateless name="Arda" :counter="counter" />
        <CounterStateless name="Guler" :counter="counter" />
        <button @click="counter++">Increment</button>
    </div>
</template>

<script setup>
import { ref } from "vue";
import Counter from "./Counter.vue";
import CounterStateless from "./CounterStateless.vue";

const counter = ref(0);
</script>

<style lang="scss" scoped></style>
