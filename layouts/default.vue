<template>
  <div class="q-layout">
    <!-- Navbar -->
    <b-navbar toggleable="lg" type="dark" variant="primary">
      <b-navbar-brand href="#">Qontak</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">ID</b-dropdown-item>
            <b-dropdown-item href="#">EN</b-dropdown-item>
          </b-nav-item-dropdown>
          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <b-icon icon="person-circle"></b-icon>
            </template>
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <!-- Sidebar -->
    <b-sidebar v-model="sidebar.isShown" bg-variant="primary" id="sidebar-no-header" aria-labelledby="sidebar-no-header-title" no-header shadow>
      <template>
        <div class="p-3">
          <nav class="mb-3">
            <b-nav vertical>
              <b-nav-item active>
                <span class="text-light">Home</span>
              </b-nav-item>
              <b-nav-item href="#link-1">
                <span class="text-light">About</span>
              </b-nav-item>
              <b-nav-item href="#link-2">
                <span class="text-light">Contact</span>
              </b-nav-item>
            </b-nav>
          </nav>
          <b-button variant="light" block @click="sidebar.isShown = !sidebar.isShown">
            <span class="text-primary">Close Sidebar</span>
          </b-button>
        </div>
      </template>
    </b-sidebar>
    <!-- Main Content -->
    <div class="q-layout__page">
      <nuxt />
    </div>
    <!-- Footer -->
    <footer class="bg-primary text-light fixed-bottom d-flex justify-content-center align-item-center p-4">
      <p class="m-0">Copyright 2022 | built by &hearts;</p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sidebar: {
        isShown: true
      }
    }
  }
}
</script>
