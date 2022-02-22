<template>
  <Link class="" :class="{ 'fw-bold': active }">
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