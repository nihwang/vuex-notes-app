<!--
1. Create new list
2. Favorite/unfavorite the currently selected note
3. Delete
-->

<template>
  <div id="toolbar">
    <i @click="addNote" clsas="glyphicon glyphicon-plus"></i>
    <i @click="toggleFavorite"
      class="glyphicon glyphicon-star"
      :class="{starred: activeNote.favorite}"></i>
    <i @click="deleteNote" class="glyphicon glyphicon-remove"></i>
  </div>
</template>

<script>
import { addNote, deleteNote, toggleFavorite } from '../vuex/actions'

export default {
  vuex: {
    getters: {
      activeNote: state => state.activeNote
    },
    actions: {
      addNote,
      delteNote,
      toggleFavorite
    }
  }
}
</script>
