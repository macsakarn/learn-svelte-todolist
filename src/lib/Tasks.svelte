<script lang="ts">
  export let tasks: string[] = []

  function _handleRemove(index){
    tasks.splice(index, 1)
    console.log(tasks);
    
    tasks=tasks
  }

</script>

{#each tasks as task, index}
  <div class="task border p-3 rounded-md my-4">
    <div class="flex justify-between">
        <input
          class="block focus:outline-none sm:text-sm w-11/12"
          name="Task"
          bind:value={task}
        />
      <img
        src="icon/icon_close.svg"
        alt="Add Icon"
        class="w-6 p-1 bg-red-600 rounded-full"
        on:click={() => _handleRemove(index)}
      />
    </div>
  </div>
{/each}
