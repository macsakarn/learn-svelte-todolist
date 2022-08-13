<script lang="ts">
  export let onClick: () => void
</script>

<button class="newTask p-3 px-5 rounded-3xl bg-purple-600" on:click={onClick}>
  <dev class="flex items-center gap-1 ">
      <img
        src="icon/icon_add.svg"
        alt="Add Icon"
        class="w-8 rounded-full"
      />
      <p class="text-white font-bold">New Task</p>
  </dev>
</button>

<style>
    .newTask{
        position: fixed;
        bottom: 0.5rem;
        left: 50%;
        transform: translate(-50%, -50%);
    }
</style>
