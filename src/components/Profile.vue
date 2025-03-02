<template>
    <h1>Profile</h1>
    <p>Name: {{ profile.name }}</p>
    <p>Email: {{ profile.email }}</p>
</template>

<script setup>
import { inject } from "vue";

const profile = inject("profile");
</script>

<style lang="scss" scoped></style>
