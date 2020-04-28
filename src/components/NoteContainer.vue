<template>
  <div class="note-container">
    <note-selectors />
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
};
</script>