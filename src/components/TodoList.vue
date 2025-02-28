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
    <div>
        <h1>TodoList</h1>
        <ul v-for="item in items" :key="item.id">
            <li v-for="(value, key) in item">
                {{ key }}: {{ value }}
            </li>
        </ul>
    </div>

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
    },
    {
        id: 2,
        text: "Learn Laravel",
    },
    {
        id: 3,
        text: "Learn Fluter",
    },
    {
        id: 4,
        text: "Learn Tailwind",
    },
];
</script>

<style lang="scss" scoped></style>
