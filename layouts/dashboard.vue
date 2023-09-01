<template>
  <div class="pb-20">
    <div :class="{'navbar' : true}">
      <div class="md:grid md:grid-cols-3 flex text-center h-full">
        <div class="flex justify-center items-center">
          <NuxtLink to="/" class="inline-flex justify-center items-center">
          <img src="../assets/img/logo.png" :class="{'logo' : !scrolled, 'scrolled-logo' : scrolled}">
          <span class="logo-text">Altify</span>
        </NuxtLink>
        </div>
        <div class="hidden md:flex justify-center items-center" />
        <LoggedInCard />
        <div class="ml-auto mr-5 md:hidden flex justify-end items-center">
          <button class="text-white text-3xl" @click="menu = !menu">
            <font-awesome-icon icon="fa-solid fa-bars" class="mx-2" />
          </button>
        </div>
      </div>
      <div :class="{'navbar-overlay' : true, 'visible' : menu}">
        <div>
          <a class="block py-3 mb-12 text-center text-2xl text-gray-400 cursor-pointer" @click="menu = !menu">close</a>
          <AltifyLogo />
          <div class="text-center my-5">
            <a href="#scroll-services" class="nav-link py-3 block">services</a>
            <a href="https://discord.gg/altify" target="_blank" class="block nav-link py-3">discord</a>
            <a href="#" class="block nav-link py-3">legal</a>
          </div>
          <ResponsiveLoggedInCard />
        </div>
      </div>
    </div>
    <Nuxt />
  </div>
</template>

<script>
import LoggedInCard from '../components/LoggedInCard.vue'

export default {
  components: { LoggedInCard },
  data () {
    return {
      scrolled: false,
      menu: false
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
.navbar {
  border-bottom: 1px solid #00b3f2;
}
</style>
