<script lang="ts">
  const primaryClasses =
    'h-8 font-normal bg-blue-600 text-blue-50 text-sm px-4 py-1 rounded-md shadow hover:bg-blue-500 active:bg-blue-700 transition-all';

  const buttonClasses = primaryClasses;
</script>

<button class={buttonClasses} type="button">
  <slot />
</button>
