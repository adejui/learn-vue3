<template>
    <div>
        <h1>Counter {{ counter.name }}: {{ counter.count }}</h1>
        <button v-on:click="increment">Increment</button>
    </div>
</template>

<script setup>
import { nextTick, ref } from "vue";

console.log("Counter Component Loaded");
let counter = ref({
    count: 0,
    name: "Ade",
});

async function increment() {
    console.log(`Increment count: ${counter.value.count}`);
    counter.value = {
        count: counter.value.count + 1,
        name: counter.value.name,
    };

    counter.value.count++;
    counter.value.count++;
    counter.value.count++;

    await nextTick();

    console.log(`Increment count after next tick: ${counter.value.count}`);
}
</script>

<style lang="scss" scoped></style>

<!-- <template>
    <div>
        <h1>Counter : {{ count }}</h1>
        <button v-on:click="increment">Increment</button>
    </div>
</template>

<script setup>
import { ref } from "vue";

console.log("Counter Component Loaded");
let count = ref(0);

function increment() {
    console.log(`Increment count:  ${count.value}`);
    count.value++;
}
</script>

<style lang="scss" scoped></style> -->
