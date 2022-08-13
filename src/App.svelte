<script lang="ts">
  import Tasks from './lib/Tasks.svelte'
  import NewTask from './lib/NewTask.svelte'

  let tasks: string[] = ["Task1","Task2","Task3"]

  function addTask() {
    tasks = [...tasks , "New Task"]
  }
</script>


<div class="mb:container mx-auto px-5">
  <p class="text-2xl font-bold text-center py-10">Todo List</p>
  <NewTask onClick={addTask} />
  <Tasks tasks={tasks} />
</div>