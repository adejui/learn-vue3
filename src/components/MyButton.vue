<template>
    <button>My Button : {{ attributes.name }}</button>
</template>

<script setup>
import { useAttrs } from "vue";

// const props = defineProps(["contoh"]);
// console.info(props);

const attributes = useAttrs();
console.log(attributes);
</script>

<style scoped></style>
