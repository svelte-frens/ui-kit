<script lang="ts">
  import Button from '$lib/button/button.svelte';
</script>

<ul class="grid grid-cols-1 gap-6 sm:grid-cols-3 lg:grid-cols-5">
  <li class="col-span-1 flex w-full items-center justify-center space-x-6 p-6">
    <Button primary>Primary button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button>Primary button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button>Primary button</Button>
  </li>
</ul>
