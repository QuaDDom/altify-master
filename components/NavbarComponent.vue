<template>
  <div :class="{'navbar' : true, 'scrolled' : scrolled}">
    <div class="md:grid md:grid-cols-3 flex text-center h-full">
      <div class="flex justify-center items-center">
        <NuxtLink to="/" class="inline-flex justify-center items-center">
          <img src="../assets/img/logo.png" :class="{'logo' : !scrolled, 'scrolled-logo' : scrolled}">
          <span class="logo-text">Altify</span>
        </NuxtLink>
      </div>
      <div class="hidden md:flex justify-center items-center">
        <a href="#scroll-services" class="nav-link">services</a>
        <a href="https://discord.gg/altify" target="_blank" class="nav-link">discord</a>
        <a href="#" class="nav-link">legal</a>
      </div>
      <div v-if="false" class="hidden md:flex justify-center items-center text-white text-xl">
        <NuxtLink to="/login" class="btn-small btn-blue mr-3" href="#scroll-services">
          Log in
        </NuxtLink>
        <NuxtLink to="/register" class="btn-small btn-secondary mr-3" href="#scroll-services">
          Sign up
        </NuxtLink>
      </div>
      <LoggedInCard v-else />
      <div class="ml-auto mr-5 md:hidden flex justify-end items-center">
        <button class="text-white text-3xl" @click="menu = !menu">
          <font-awesome-icon icon="fa-solid fa-bars" class="mx-2" />
        </button>
      </div>
    </div>
    <div :class="{'navbar-overlay' : true, 'visible' : menu}">
      <div>
        <a class="block py-3 mb-6 text-center text-2xl text-gray-400 cursor-pointer" @click="menu = !menu">close</a>
        <AltifyLogo />
        <div class="text-center my-5">
          <NuxtLink :to="'/' + '#scroll-services'" class="nav-link py-3 block">
            services
          </NuxtLink>
          <NuxtLink to="https://discord.gg/altify" target="_blank" class="block nav-link py-3">
            discord
          </NuxtLink>
          <NuxtLink to="#" class="block nav-link py-3">
            legal
          </NuxtLink>
          <NuxtLink to="/cart" class="block nav-link py-3">
            cart
          </NuxtLink>
        </div>
        <ResponsiveLoggedInCard />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      scrolled: false,
      menu: false
    }
  },
  watch: {
    $route (to, from) {
      this.menu = false
    }
  },
  beforeMount () {
    window.addEventListener('wheel', this.scrollFunc)
  },
  beforeDestroy () {
    window.removeEventListener('wheel', this.scrollFunc)
  },
  methods: {
    scrollFunc (event) {
      this.scrolled = window.scrollY > 50
    }
  }
}

</script>

<style scoped>
.navbar-overlay {
  position: fixed;
  width: 100%;
  height: 100vh;
  top: 0; left: 0;
  background: #121619;
  @apply flex justify-center items-center;
  opacity: 0;
  transition: all .3s;
  visibility: hidden;
}

.visible {
  opacity: 1 !important;
  visibility: visible !important;
}

.nav-link {
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    color: #ffffff;
    @apply mx-3;
    transition: all .1s;
}
.nav-link:hover {
    color: #007bd2;
}

.navbar {
    z-index: 100;
    width: 100%;
    height: 6em;
    background-color: #121619;
    position: fixed;
    transition: all .3s;
    filter: drop-shadow(0px 7px 10px rgba(0, 0, 0, 0.25));
}
.scrolled {
    height: 5em;
}
.logo {
    width: 75px;
    transition: all .3s;
    height: 75px;
}
.scrolled-logo {
    transition: all .3s;
    width: 60px;
    height: 60px;
}
.logo-text {
    font-family: 'Ubuntu';
    font-style: normal;
    font-weight: 600;
    font-size: 32px;
    color: #FFFFFF;
}
</style>
