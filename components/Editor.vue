<!--
  1. Grabs current activeNote from the store and displays it in a text area
  2. It calls the editNote() action whenever the user updates the note
 -->

 <template>
   <div id="note-editor">
     <textarea
      :value="activeNoteText"
      @input="editNote"
      class="form-control">
     </textarea>
   </div>
 </template>

 <script>
 import { editNote } from '../vuex/actions'

 export default {
  vuex: {
    getters: {
      activeNoteText: state => state.activeNote.text
    },
    actions: {
      editNote
    }
  }
 }
 </script>
