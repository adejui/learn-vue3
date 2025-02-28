<template>
    <div>
        <h1>Score App</h1>
        <div v-show="score > 99">
            <p>score is {{ score }}</p>
        </div>
        <div v-if="score > 90">
            <p>Congratulations! Your score is {{ score }}.</p>
        </div>
        <div v-else-if="score > 70">
            <p>You have passed the exam! Your score is {{ score }}</p>
        </div>
        <div v-else>
            <p>Sorry, you failed the exam. Your score is {{ score }}</p>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";

const score = ref(98);
</script>

<style lang="scss" scoped></style>
