<script lang="ts">
  import Button from '$lib/button/button.svelte';
</script>

<ul class="grid grid-cols-1 gap-6 sm:grid-cols-3 lg:grid-cols-4">
  <!-- Large -->
  <li class="col-span-1 flex w-full items-center justify-center space-x-6 p-6">
    <Button primary size={'large'}>Primary button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button size={'large'}>Default button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button text size={'large'}>Text button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button link size={'large'}>Link button</Button>
  </li>

  <!-- Medium -->
  <li class="col-span-1 flex w-full items-center justify-center space-x-6 p-6">
    <Button primary>Primary button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button>Default button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button text>Text button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button link>Link button</Button>
  </li>

  <!-- Small -->
  <li class="col-span-1 flex w-full items-center justify-center space-x-6 p-6">
    <Button primary size={'small'}>Primary button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button size={'small'}>Default button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button text size={'small'}>Text button</Button>
  </li>
  <li class="col-span-1 flex w-full items-center justify-between space-x-6 p-6">
    <Button link size={'small'}>Link button</Button>
  </li>
</ul>
