<script lang="ts">

  import Badge from './Badge.svelte';

  let { title = "Project Title", description = "This is a brief description of the project.", techSkills = [], url=""} = $props();

</script>

 <div class="col-span-1 rounded-md border px-2 py-1 flex flex-col justify-stretch">
    <div class="h-48"><img src="/{url}" /></div>
    <div class="grow flex flex-col justify-between">  
      <div class="">
        <p class="text-lg">{title}</p>
        <p class="text-md mt-1">{description}</p>
      </div>
      <div class="flex flex-wrap items-start gap-1 pb-1">
        {#each techSkills as skill}
          <Badge label={skill} size="small" />
        {/each}
      </div>
    </div>
  </div>

