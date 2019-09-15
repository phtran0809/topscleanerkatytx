<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <a href="tel:(281) 693-6002">
              <i class="fas fa-phone"></i> (281) 693-6002
            </a>
          </li>
          <li>
            <a class="nav-link" href="https://goo.gl/maps/PE3PjYJ4xe3oFkz86" target="_blank">
              <i class="now-ui-icons location_map-big"></i> 23106 Cinco Ranch Blvd, Katy, TX 77494
            </a>
          </li>
          
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }} TopsCleaner
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>
