<template>
    <div>
        <h1>counter {{ name }} : {{ counter }}</h1>
        <button @click="$emit('click', increment)">Increment {{ name }}</button>
    </div>
</template>

<script setup>
const { counter, name, increment } = defineProps({
    counter: Number,
    name: String,
    increment: Number,
});

defineOptions({
    inheritAttrs: false,
});
// const emits = defineEmits(["click"]);

// function buttonClick() {
//     emits("click", increment);
// }
</script>

<style lang="scss" scoped></style>
