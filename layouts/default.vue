<template>
  <div class="q-layout">
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
