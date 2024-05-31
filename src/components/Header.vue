<template>
  <header class="tilt">
    <div class="container d-flex justify-content-center p-1">
      <nav class="navbar navbar-expand-lg navbar-dark ">
        <div class="container">
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown"
            aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNavDropdown">
            <ul class="navbar-nav">
              <li class="nav-item active mx-1">
                <router-link class="nav-link" to="/">Home <span class="sr-only">(current)</span></router-link>
              </li>
              <li class="nav-item" mx-1>
                <router-link class="nav-link" to="/portfolio">Portfolio</router-link>
              </li>
              <li class="nav-item mx-1">
                <router-link class="nav-link" to="/blog">Blog</router-link>
              </li>
              <li class="nav-item dropdown">
                <router-link to="/services" class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink"
                  data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                  Services
                </router-link>
                <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                  <router-link to="/service1" class="dropdown-item nav-link" href="#">Service 1</router-link>
                  <router-link to="/service2" class="dropdown-item nav-link" href="#">Service 2</router-link>
                  <router-link to="/service3" class="dropdown-item nav-link" href="#">Service 1</router-link>
                </div>
              </li>
              <li class="nav-item mx-1">
                <router-link class="nav-link" to="/testimonials ">Testimonials</router-link>
              </li>
              <li class="nav-item mx-1">
                <router-link class="nav-link" to="/contact">contact us</router-link>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style>
.tilt {
  background-color: #1e012c;
  box-shadow: 0px 0px 30px rgba(227, 228, 237, 0.37);
  border: 2px solid rgba(255, 255, 255, 0.18);
  position: fixed;
  bottom: 0;
  width: 100%;
  z-index: 2;
  font-size: xx-large;
}
</style>
