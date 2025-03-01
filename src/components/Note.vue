<template>
    <div>
        <h1>Buat Note</h1>
        <input ref="noteInput" type="text" name="note" v-model="note" placeholder="Tulis Note Disini" autofocus/>
        <button @click="addNote">Tambah note</button>
    </div>

    <h1>Daftar Note</h1>
    <ul>
        <li v-for="note in notes" ref="noteList">{{ note }}</li>
    </ul>
</template>

<script setup>
import { reactive, useTemplateRef, ref } from "vue";

const notes = reactive([]);
const note = ref("");
const noteInput = useTemplateRef("noteInput");
const noteList = useTemplateRef("noteList");

function addNote() {
    notes.push(note.value);
    note.value = "";
    noteInput.value.focus();
    if(noteList.value) {
        noteList.value.forEach((li) => {
            console.log(li.textContent);
        })
    }
}
</script>

<style lang="scss" scoped></style>
