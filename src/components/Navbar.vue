<template>
<nav class="navbar has-border" role="navigation" aria-label="main navigation">
  <div class="container">
<div class="navbar-brand">
    <g-link class="navbar-item" to="/">
      Company Logo
    </g-link>
    <a 
    role="button" 
    class="navbar-burger burger" 
    :class="{ 'is-active': showNav }"
    aria-label="menu"
    aria-expanded="false"
    @click="showNav = !showNav"
    >
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div  
  class="navbar-menu"
  :class="{ 'is-active': showNav } "
  >

    <div class="navbar-start">
      <g-link to="/pages/gate" class="navbar-item">
        GATE
      </g-link>
      <g-link to="/pages/psu" class="navbar-item">
        PSUs
      </g-link>
      <g-link to="/pages/crt" class="navbar-item">
        CRT
      </g-link>
    </div>

    <div class="navbar-end">
      <g-link to="/" class="navbar-item">
        Home
      </g-link>
      <g-link to="/Notifications" class="navbar-item">
        News
      </g-link>
      <g-link to="/Contact" class="navbar-item">
        Contact
      </g-link>
    </div>

    </div>
  </div>
</nav>
</template>

<script>
export default {
    data: () => ({
    showNav: false,
  }),
}
</script>

<style scoped>
.navbar-item img {
    max-height: unset;
}
img {
  max-width: unset;
  height: unset;
}

.navbar-item {
  margin-bottom: -1px;
  border-bottom: 1px solid transparent;
  font-weight: 300;
}
.navbar-item.active--exact {
  color: #000;
  font-weight: 400;
  font-weight: medium;
}
@media only screen and (min-width: 768px) {
.navbar-item.active--exact {
  border-bottom: 1px solid #4a4a4a;
}
}
.navbar-brand .navbar-item.active--exact{
  font-weight: normal;
  border-bottom: 1px solid transparent;
}
.navbar-item:hover, .navbar-item:focus {
  background: transparent;
}
.navbar.has-border {
  border-bottom:1px solid #ededed;
}
.navbar-burger {
    height: 4.75rem;
}
</style>