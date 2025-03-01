<template>
    <h1>counter {{ name }} : {{ counter }}</h1>
</template>

<script setup>
const { counter, name } = defineProps(["counter", "name"]);
</script>

<style lang="scss" scoped></style>
