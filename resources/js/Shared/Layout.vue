<template>
  <div class="header bg py-2">
    <div class="container text-white">
      <div class="row pb-5">
        <div class="col-6">Hello.</div>
        <div class="col-6 text-end">555 899-1212</div>
      </div>
      <!--/row-->
    </div>
    <!--container-->
  </div>
  <span class="position-absolute trigger">
    <!-- hidden trigger to apply 'stuck' styles -->
  </span>

  <Nav />

  <div class="container-fluid">
    <br />
    <slot />
  </div>
</template>

<script>
import Nav from "./Nav.vue";

export default {
  components: { Nav },

  mounted() {
    new IntersectionObserver(function (e, o) {
      if (e[0].intersectionRatio > 0) {
        document.documentElement.removeAttribute("class");
      } else {
        document.documentElement.setAttribute("class", "stuck");
      }
    }).observe(document.querySelector(".trigger"));
  },
};
</script>