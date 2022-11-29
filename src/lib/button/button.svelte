<script lang="ts">
  /**
   * Button types
   */
  export let primary = false;
  export let text = false;
  export let link = false;

  const commonClasses = 'box-border whitespace-nowrap shadow-sm';

  const primaryTypeClasses =
    commonClasses +
    'h-8 font-normal bg-blue-600 text-blue-50 text-sm px-4 py-1 rounded-md hover:bg-blue-500 active:bg-blue-700 transition-all';

  const defaultTypeClasses =
    commonClasses +
    `h-8 font-normal bg-white border-gray-300 border text-sm text-gray-900 px-4 py-1 rounded-md hover:border-blue-500 hover:text-blue-500 active:border-blue-700 active:text-blue-700 transition-all`;

  const buttonClasses = primary ? primaryTypeClasses : defaultTypeClasses;
</script>

<button class={buttonClasses} type="button">
  <slot />
</button>
