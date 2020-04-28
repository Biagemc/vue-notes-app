<template>
  <div class="note-selectors">
    <note-selector
      v-for="note in notes"
      v-bind:key="note.id"
      v-bind:note="note"
      v-bind:selectedNoteId="selectedNoteId"
      v-on:selectNote="selectNote"
    />
  </div>
</template>

<script>
import noteSelector from "./NoteSelector.vue";

export default {
  name: "note-selectors",
  components: {
    noteSelector,
  },
  data: function() {
    return {};
  },
  props: ["notes", "selectedNoteId"],

  methods: {
    selectNote: function(note) {
      this.$emit("selectNote", note);
    },
  },
};
</script>
