<template>
  <b-navbar
    sticky
    toggleable="lg"
    type="dark"
    variant="primary"
    class="d-flex justify-content-start"
  >
    <b-navbar-toggle target="nav-collapse" class="m-0 p-0">
      <MenuIcon />
    </b-navbar-toggle>

    <b-navbar-brand class="ml-2" @click="$router.push('/')" style="cursor: pointer;">
      <logo />
    </b-navbar-brand>

    <b-navbar-toggle target="search-collapse" class="ml-auto m-0 p-0">
      <searchIcon />
    </b-navbar-toggle>

    <b-collapse
      id="nav-collapse"
      v-model="menuVisible"
      style="flex-grow: initial!important;"
      class="ml-auto"
      is-nav
    >
      <b-navbar-nav>
        <b-nav-item href="#">
          <TrendingIcon :size="20" />
          <span>Trending</span>
        </b-nav-item>
        <b-nav-item href="#">
          <TopIcon :size="20" />
          <span>Top</span>
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>

    <b-collapse id="search-collapse" class="flex-grow-1" is-nav>
      <b-navbar-nav class="mx-auto flex-fill" style="max-width: 700px;">
        <b-input placeholder="Discover Topics . . ."></b-input>
      </b-navbar-nav>
    </b-collapse>

    <b-collapse
      id="nav-collapse"
      v-model="menuVisible"
      style="flex-grow: initial!important;"
      is-nav
    >
      <!-- Right Aligned Nav Items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item>
          <b-button variant="outline-light" block squared size="sm" to="register">Register</b-button>
        </b-nav-item>
        <b-nav-item>
          <b-button variant="danger" block squared size="sm" to="login">Login</b-button>
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
import logo from '~/components/core/logoFull'

// Icons
import LoginIcon from 'vue-material-design-icons/LoginVariant.vue'
import TrendingIcon from 'vue-material-design-icons/Fire.vue'
import TopIcon from 'vue-material-design-icons/FormatListNumbered.vue'
import MenuIcon from 'vue-material-design-icons/Menu.vue'
import searchIcon from 'vue-material-design-icons/Magnify.vue'

export default {
  name: 'appBar',
  components: {
    LoginIcon,
    TrendingIcon,
    TopIcon,
    MenuIcon,
    logo,
    searchIcon
  },
  data() {
    return {
      menuVisible: false
    }
  }
}
</script>

<style scoped>
</style>
