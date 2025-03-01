<template>
    <div v-if="slots.header">
        <slot name="header" :counter="counter">
            <h1>Anda belum Mengisi Header</h1>
        </slot>
    </div>
    <div v-if="slots.default">
        <slot name="default" :counter="counter">
            <p>Anda belum Mengisi kontennya</p>
        </slot>
    </div>
    <div v-if="slots.footer">
        <slot name="footer" :counter="counter">
            <h4>Anda belum Mengisi Footer</h4>
        </slot>
    </div>
    <div>
        <button @click="counter++">Increment</button>
    </div>
</template>

<script setup>
import { ref, useSlots } from "vue";

const slots = useSlots();
const counter = ref(0);
</script>

<style lang="scss" scoped></style>
