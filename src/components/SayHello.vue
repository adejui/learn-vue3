<template>
    <div>
        <button v-on:click="increment">Increment {{ counter }}</button> <br />
        <input type="text" id="firstName" placeholder="First Name" /> <br />
        <input type="text" id="lastName" placeholder="Last Name" /> <br />

        <button v-on:click="sayHello">Say Hello</button>

        <h1>Hello {{ fullName }}</h1>
    </div>
</template>

<script setup>
import { computed, reactive, ref } from "vue";

const person = reactive({
    firstName: "",
    lastName: "",
});

function sayHello() {
    person.firstName = document.getElementById("firstName").value;
    person.lastName = document.getElementById("lastName").value;
}

const fullName = computed((oldName) => {
    console.log(`${oldName}`);
    return `${person.firstName} ${person.lastName}`;
});

const counter = ref(0);

function increment() {
    console.log(`increment called`);
    counter.value++;
}
</script>

<style lang="scss" scoped></style>
