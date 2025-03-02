<template>
    <input type="text" v-model="profile.name" placeholder="Name" />
    <Profile />
    <ProfileAddress />
</template>

<script setup>
import { provide, reactive } from "vue";
import Profile from "./Profile.vue";
import ProfileAddress from "./ProfileAddress.vue";

const profile = reactive({
    name: "Ade",
    email: "test@gmail.com",
});

provide("profile", profile);
</script>

<style lang="scss" scoped></style>
