<script lang="ts">
  import type { BUTTON_SIZE } from './button.type';

  // Button types
  export let primary = false;
  export let text = false;
  export let link = false;
  // Button size
  export let size: BUTTON_SIZE = 'medium';
  // States
  export let disabled = false;

  const commonClasses = 'box-border whitespace-nowrap';
  const commonDisabledClasses = `hover:cursor-default text-gray-600`;

  /**
   * Button sizes
   */
  const smallSizeClasses = `h-6 text-sm py-0 px-2 rounded`;
  const mediumSizeClasses = `h-8 text-sm font-normal py-1 px-4 rounded-md`;
  const largeSizeClasses = `h-10 text-base font-normal py-2 px-4 rounded-lg`;

  /**
   * Button types
   */
  const primaryTypeClasses =
    'bg-blue-600 text-blue-50 hover:bg-blue-500 active:bg-blue-700 transition-all shadow-sm';
  const defaultTypeClasses = `bg-white border-gray-300 border text-gray-900 hover:border-blue-500 hover:text-blue-500 active:border-blue-700 active:text-blue-700 transition-all shadow-sm`;
  const textTypeClasses =
    'bg-transparent text-gray-900 hover:bg-gray-100 active:bg-gray-300 transition-all';
  const linkTypeClasses =
    'bg-transparent text-blue-600 hover:underline hover:text-blue-400 active:text-blue-700 transition-all';

  /**
   * Disabled classes
   */
  const primaryTypeDisabledClasses = `${commonDisabledClasses} bg-blue-200`;
  const defaultTypeDisabledClasses = `${commonDisabledClasses} border-gray-300 text-gray-600`;
  const textTypeDisabledClasses = `${commonDisabledClasses}`;

  /**
   * Class wrangling
   */
  const buttonTypeClasses = primary
    ? primaryTypeClasses
    : text
    ? textTypeClasses
    : link
    ? linkTypeClasses
    : defaultTypeClasses;

  const buttonSizeClasses =
    size === 'small'
      ? smallSizeClasses
      : size === 'large'
      ? largeSizeClasses
      : mediumSizeClasses;

  const disabledClasses = disabled
    ? primary
      ? primaryTypeDisabledClasses
      : text
      ? textTypeDisabledClasses
      : defaultTypeDisabledClasses
    : '';

  const buttonClasses = `${commonClasses} ${buttonTypeClasses} ${buttonSizeClasses}`;
</script>

<button class={`${buttonClasses}${disabledClasses}`} type="button" {disabled}>
  <slot />
</button>
