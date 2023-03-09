<script>
	import NoteForm from './NoteForm.svelte';
	import NoteList from './NoteList.svelte';

let notes = [];

function saveNote(note) {
  notes = [...notes, note];
}

function deleteNote(index) {
  notes = notes.filter((_, i) => i !== index);
}


</script>



<style>
	.app-head {
		color: black;
		background-color: lightskyblue;
		
	}

	.flex-app {
		display: flex;
	}
</style> 

 <h1 class="app-head">Inkwell</h1>

<div class="flex-app">
	<div>
		<NoteList notes={notes} onDelete={deleteNote} />
	</div>
	<div>
		<NoteForm onSave={saveNote} />
	</div>
</div>
