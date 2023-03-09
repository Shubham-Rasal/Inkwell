<script>
    export let notes = [];
    export let onDelete;

function deleteNote(index) {
  onDelete(index);
}
</script>


<style>

  .notehead{
    background-color: white;
    color: black;
    border: 2px solid #4CAF50;
    margin: 3px 3px;
  }
  .notehead:hover {
    cursor: pointer;
    background-color: #4CAF50; /* Green */
    color: white;
    box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
  }

  .notehead button {
    background-color: white;
    color: black;
    border-radius: 20px;
  }

  .notehead button:hover {
    cursor: pointer;
  }
</style>
<ul>
    {#each notes as note, i}
      <button class="notehead">
        { note}
        <button on:click={() => deleteNote(i)}>X</button>
      </button>
    {/each}
  </ul>