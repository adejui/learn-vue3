<template>
    <MyButton class="button" @click="clickHandler" name="Ade" contoh="Jui" />
</template>

<script setup>
import MyButton from "./MyButton.vue";

function clickHandler() {
    alert("You Click Me");
}
</script>

<style scoped>
.button {
    display: inline-block;
    padding: 12px 24px;
    font-size: 16px;
    font-weight: bold;
    color: white;
    background: linear-gradient(135deg, #007bff, #00d4ff);
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
    box-shadow: 0 4px 10px rgba(0, 123, 255, 0.3);
}

.button:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(0, 123, 255, 0.4);
}

.button:active {
    transform: translateY(0);
    box-shadow: 0 3px 8px rgba(0, 123, 255, 0.3);
}
</style>
