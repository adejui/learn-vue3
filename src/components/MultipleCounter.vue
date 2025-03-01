<template>
    <div>
        <Counter name="Ade" initial-count="100" />
        <Counter name="Jui" initial-count="100" />

        <CounterStateless name="Arda" :counter="counter" @click="increment" :increment="1" />
        <CounterStateless name="Guler" :counter="counter" @click="increment" :increment="2" />
        <button @click="counter++">Increment</button>
    </div>
</template>

<script setup>
import { ref } from "vue";
import Counter from "./Counter.vue";
import CounterStateless from "./CounterStateless.vue";

const counter = ref(0);

function increment(value) {
    counter.value += value;
}
</script>

<style lang="scss" scoped></style>
