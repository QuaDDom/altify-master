<template>
  <div>
    <div class="div-centering full-size px-5 my-5 md:my-0">
      <div>
        <AltifyLogo />
        <div class="md:div-centering">
          <div class="my-6">
            <h1 class="login-title">
              Sign up with Discord
            </h1>
            <p class="login-description text-gray-400 mb-4">
              Use Discord for quick authentication and identification on our Discord server!
            </p>
            <a class="btn btn-blue" href="#" target="_blank">
              Sign up with Discord
            </a>
          </div>
          <div class="separator hidden md:block" />
          <div>
            <h1 class="login-title">
              No Discord?
            </h1>
            <p class="login-description text-gray-400 mb-4">
              We strongly recommend you using a Discord account for quick authentication but if it isn't an option for you, you can register anyway.
            </p>
            <form action="" method="post">
              <div v-if="incorrect" class="incorrect-label">
                These credentials don't match any account
              </div>
              <input type="text" :class="{'login-input' : true, 'incorrect' : incorrect}" placeholder="Enter your username" required>
              <input type="email" :class="{'login-input' : true, 'incorrect' : incorrect}" placeholder="Enter your email" required>
              <input type="password" placeholder="Enter your password" :class="{'login-input' : true, 'incorrect' : incorrect}" required>
              <input type="password" placeholder="Confirm your password" :class="{'mb-6 login-input' : true, 'incorrect' : incorrect}" required>
              <a class="btn btn-secondary" href="#" target="_blank">
                Sign up
              </a>
            </form>
            <div class="mt-6">
              <NuxtLink to="/login" class="nav-link block md:inline-block">
                Already have an account?
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RegisterPage',
  data () {
    return {
      incorrect: false
    }
  }
}
</script>

<style>
</style>
