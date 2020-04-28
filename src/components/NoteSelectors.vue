<template>
  <div class="note-selectors">
    <note-selector class="active" />
    <note-selector />
    <note-selector />
  </div>
</template>

<script>
import noteSelector from "./NoteSelector.vue";

export default {
  name: "note-selectors",
  components: {
    noteSelector,
  },
};
</script>