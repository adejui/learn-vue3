<template>
    <h1 :id v-bind:class="classHello">{{ hello }}</h1>

    <h1 v-bind="data" v-html="hello"></h1>

    <h1 :class="data.class">{{ hello.toUpperCase() }}</h1>

    <h3>{{ 200 * 20 }}</h3>

    <div>{{ helloWorld() }}</div>

    <div :class="classHello" v-html="hello"></div>

    <button :disabled="buttonDisabled">this is button</button>
</template>

<script setup>
function helloWorld() {
    return "Hello world!";
}

console.info("Hello Vue");

const hello = "<h1>Hello Vue</h1>";
const classHello = "hello";
const id = "hello";
const buttonDisabled = true;

const data = {
    class: "hello",
    id: "hello",
};
</script>

<style scoped>
.hello {
    color: green;
}
</style>
