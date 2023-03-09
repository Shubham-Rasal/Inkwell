<script>

export let onSave;
export let headNote;

let note = '';

function saveNote() {
  onSave(note);
  note = '';
}

function noteHead() {
  headNote(note)
}
</script>


<form on:submit|preventDefault={saveNote}>
    <textarea rows="20" cols="50" bind:value={note}></textarea>
    <button type="submit">Save</button>
  </form>