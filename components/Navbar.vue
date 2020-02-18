  
<template>
    <div class="navigation">
        
        <nav class="navbar" v-bind:class="{ hidden: !isOpen, 'navbar-white': isOpen }" role="navigation" aria-label="main navigation">
          <div class="navbar-brand">

            <a class="brand-item" href="/">
              <!--<img class="logo"  alt="Logo" src="/logo.svg">-->
            </a>

            <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" @click="isOpen = !isOpen" v-bind:class="{'is-active': isOpen}">
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
              <span aria-hidden="true"></span>
            </a>
          </div>

          <div class="navbar-menu" v-bind:class="{'is-active': isOpen}">
            <div class="navbar-end">
              <nuxt-link to="/" class="navbar-item">
                Kezdőoldal
              </nuxt-link>

              <nuxt-link to="/rolunk" class="navbar-item">
                Rólunk 
              </nuxt-link>

              <nuxt-link :to="{ path: '/', hash:'#pillanatok'}" class="navbar-item" @click="isOpen = false">
                Pillanatok
              </nuxt-link>

              <!--
              <a href="/" class="navbar-item">
                Partnereink
              </a>
              -->

              <nuxt-link to="/contact" class="navbar-item">
                Árajánlat
              </nuxt-link>

              <a href="https://www.facebook.com/nagyrichardphoto/" class="navbar-item">
                <span class="icon is-medium">
                  <font-awesome-icon :icon="['fab', 'facebook-f']"/>
                </span>
              </a>

              <a href="https://www.instagram.com/nagyrichardphoto/" class="navbar-item">
                <font-awesome-icon :icon="['fab', 'instagram']"/>
              </a>

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

.navbar-white {
  background-color: white !important;
}

</style>
