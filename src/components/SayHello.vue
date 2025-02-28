<template>
    <form action="">
        <div>
            <button v-on:click="counter++">Increment {{ counter }}</button> <br />
            <input type="text" id="firstName" placeholder="First Name" @input="changeFirstName" /> <br />
            <input type="text" id="lastName" placeholder="Last Name" @input="changeLastName" /> <br />

            <button v-on:click.prevent="sayHello">Say Hello</button>

            <h1>Hello {{ fullName }}</h1>
        </div>
    </form>
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

function changeFirstName(event) {
    person.firstName = event.target.value;
}
function changeLastName(event) {
    person.lastName = event.target.value;
}

const counter = ref(0);

// function increment() {
//     console.log(`increment called`);
//     counter.value++;
// }
</script>

<style lang="scss" scoped></style>
