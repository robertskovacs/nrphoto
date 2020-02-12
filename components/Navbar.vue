<template>
    <div class="navigation">

      <nav class="navbar" v-bind:class="{ hidden: !isOpen}" role="navigation" aria-label="main navigation">
        <div class="container">
          <div class="navbar-brand">
            <a class="navbar-item" href="/">
              <!--<img src="https://bulma.io/images/bulma-type-white.png" alt="Logo">-->
              <p>NR Photo</p>
            </a>
            <span role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" @click="isOpen = !isOpen" v-bind:class="{'is-active': isOpen}">
              <span></span>
              <span></span>
              <span></span>
            </span>
          </div>
          <div id="navbarMenuHeroA" class="navbar-menu">
            <div class="navbar-end">
              <a href="/contact" class="navbar-item contact-link">
                Contact
              </a>
        
            </div>
          </div>
        </div>
      </nav>
        
    </div>
</template>

<script>
export default {
  name: 'Navbar',
  data: function() {
    return {
        isOpen: false
    }
  }
}
</script>

<style lang="scss">
.logo {
  height:50px;
}
</style>
