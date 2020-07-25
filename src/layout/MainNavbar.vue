<template>
  <navbar
    position="fixed"
    type="primary"
    :transparent="transparent"
    :color-on-scroll="colorOnScroll"
    menu-classes="ml-auto"
  >
    <template slot-scope="{ toggle, isToggled }">
      <router-link v-popover:popover1 class="navbar-brand" to="/">
        <img class="logo" src="img/logo-name.png" alt="Tops Cleaners" />
      </router-link>
      <!-- <el-popover
        ref="popover1"
        popper-class="popover"
        placement="bottom"
        width="200"
        trigger="hover"
      >
        <div class="popover-body">
          Designed by Invision. Coded by Creative Tim
        </div>
      </el-popover> -->
    </template>
    <template slot="navbar-menu">
      <li class="nav-item">
        <a
          class="nav-link"
          href="https://goo.gl/maps/PE3PjYJ4xe3oFkz86"
          target="_blank"
        >
          <i class="now-ui-icons location_map-big"></i>
          <p>Direction</p>
        </a>
      </li>
      <li class="nav-item">
        <a
          class="nav-link"
          href="#hours"
        >
          <i class="now-ui-icons ui-2_time-alarm"></i>
          <p>Hours</p>
        </a>
      </li>
      <!-- <drop-down
        tag="li"
        title="Components"
        icon="now-ui-icons design_app"
        class="nav-item"
      >
        <nav-link to="/">
          <i class="now-ui-icons business_chart-pie-36"></i> All components
        </nav-link>
        <a
          href="https://demos.creative-tim.com/vue-now-ui-kit/documentation"
          target="_blank"
          class="dropdown-item"
        >
          <i class="now-ui-icons design_bullet-list-67"></i> Documentation
        </a>
      </drop-down> -->
      <!-- <drop-down
              tag="li"
              title="Examples"
              icon="now-ui-icons design_image"
              class="nav-item"
      >
        <nav-link to="/topsCleaners">
          <i class="now-ui-icons education_paper"></i> topsCleaners
        </nav-link>
        <nav-link to="/login">
          <i class="now-ui-icons users_circle-08"></i> Login
        </nav-link>
        <nav-link to="/profile">
          <i class="now-ui-icons users_single-02"></i> Profile
        </nav-link>
      </drop-down> -->

      
    </template>
  </navbar>
</template>

<script>
import { DropDown, NavbarToggleButton, Navbar, NavLink } from '@/components';
import { Popover } from 'element-ui';
export default {
  name: 'main-navbar',
  props: {
    transparent: Boolean,
    colorOnScroll: Number
  },
  components: {
    DropDown,
    Navbar,
    NavbarToggleButton,
    NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style scoped></style>
