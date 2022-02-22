<template>
  <!-- <nav>
    <ul class="flex space-x-6">
      <li>
        <NavLink href="/" :active="$page.component === 'Home'">Home</NavLink>
      </li>
      <li>
        <NavLink href="/users" :active="$page.component === 'Users'"
          >Users</NavLink
        >
      </li>
      <li>
        <NavLink href="/settings" :active="$page.component === 'Settings'"
          >Settings</NavLink
        >
      </li>
    </ul>
  </nav> -->

  <nav class="navbar navbar-expand-sm sticky-top navbar-dark bg-info py-4">
    <div class="collapse navbar-collapse" id="navbar1">
      <ul class="navbar-nav">
        <li class="nav-item">
          <NavLink
            class="nav-link"
            href="/"
            :active="$page.component === 'Home'"
            >Home</NavLink
          >
        </li>
        <li class="nav-item">
          <NavLink
            class="nav-link"
            href="/users"
            :active="$page.component === 'Users'"
            >Users</NavLink
          >
        </li>
        <li class="nav-item">
          <NavLink
            class="nav-link"
            href="/settings"
            :active="$page.component === 'Settings'"
            >Settings</NavLink
          >
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import NavLink from "./NavLink.vue";

export default {
  components: { NavLink },
};
</script>
