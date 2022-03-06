<template>
  <div class="q-layout">
    <!-- Sidebar -->
    <b-sidebar v-model="sidebar.isShown" id="sidebar-no-header" aria-labelledby="sidebar-no-header-title" no-header shadow>
      <template>
        <div class="p-3">
          <h4 id="sidebar-no-header-title">Custom header sidebar</h4>
          <p>
            Cras mattis consectetur purus sit amet fermentum. Cras justo odio, dapibus ac facilisis
            in, egestas eget quam. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.
          </p>
          <nav class="mb-3">
            <b-nav vertical>
              <b-nav-item active @click="hide">Active</b-nav-item>
              <b-nav-item href="#link-1" @click="hide">Link</b-nav-item>
              <b-nav-item href="#link-2" @click="hide">Another Link</b-nav-item>
            </b-nav>
          </nav>
          <b-button variant="primary" block @click="sidebar.isShown = !sidebar.isShown">Close Sidebar</b-button>
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
