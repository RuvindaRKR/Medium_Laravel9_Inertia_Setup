<template>
  <Link
    class="text-black-500 hover:underline"
    :class="{
      'block py-2 pr-4 pl-3 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white':
        active,
    }"
    aria-current="page"
  >
    <slot />
  </Link>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";
export default {
  props: {
    active: Boolean,
  },

  components: { Link },
};
</script>