<template>
    <div>
        <h1>TodoList</h1>
        <ul>
            <li v-for="item in items">
                {{ item.id }}.
                {{ item.text }}
            </li>
        </ul>
    </div>

    <h1>TodoList</h1>
    <template v-for="item in items">
        <ul v-if="!item.done" :key="item.id">
            <li v-for="(value, key) in item">{{ key }}: {{ value }}</li>
        </ul>
    </template>

    <div>
        <div v-for="n in 10">
            <p>Hello {{ n }}</p>
        </div>
    </div>
</template>

<script setup>
const items = [
    {
        id: 1,
        text: "learn Vue 3",
        done: true,
    },
    {
        id: 2,
        text: "Learn Laravel",
        done: false,
    },
    {
        id: 3,
        text: "Learn Fluter",
        done: false,
    },
    {
        id: 4,
        text: "Learn Tailwind",
        done: false,
    },
];
</script>

<style lang="scss" scoped></style>
