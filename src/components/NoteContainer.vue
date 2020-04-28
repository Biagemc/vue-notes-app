<template>
  <div class="note-container">
    <note-selectors v-bind:notes="notes" v-on:selectNote="selectNote" v-bind:selectedNoteId="selectedNoteId" />
    <note-editor />
  </div>
</template>

<script>
import noteSelectors from "./NoteSelectors.vue";
import noteEditor from "./NoteEditor.vue";

export default {
  name: "note-container",
  components: {
    noteSelectors,
    noteEditor,
  },
  props: ["notes", "selectedNoteId"],
  methods: {
    selectNote: function(note) {
      this.$emit("selectNote", note);
    },
  },
};
</script>
