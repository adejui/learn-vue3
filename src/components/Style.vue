<template>
    <div>
        <h1 :class="{ redd: red, bold: bold }">style</h1>
        <h1 :class="array">style</h1>
        <h1 :style="style1">Style</h1>
        <h1 :style="style2">Style</h1>
        <h1 :style="[style1, style2]">Style</h1>
        <h1 :style="{ style1: red, style2: bold }">Style</h1>
        <button v-on:click="toggleRed">Red</button>
        <button v-on:click="toggleBold">Bold</button>
    </div>
</template>

<script setup>
import { ref } from "vue";

const array = ["red", "bold"];

const red = ref(false);
const bold = ref(false);

function toggleRed() {
    red.value = !red.value;
}

function toggleBold() {
    bold.value = !bold.value;
}

const style1 = {
    color: "red",
};
const style2 = {
    textTransform: "uppercase",
    fontWeight: "bold",
};
</script>

<style scoped>
.redd {
    color: red;
}

.bold {
    text-transform: uppercase;
    font-weight: bold;
}
</style>
