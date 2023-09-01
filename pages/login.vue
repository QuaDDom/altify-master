<template>
  <div>
    <div class="div-centering full-size px-5 my-5 md:my-0">
      <div>
        <AltifyLogo />
        <div class="md:div-centering">
          <div class="my-6">
            <h1 class="login-title">
              Login with Discord
            </h1>
            <p class="login-description text-gray-400 mb-4">
              Use Discord for quick authentication and identification on our Discord server!
            </p>
            <a class="btn btn-blue" href="#" target="_blank">
              Log in with Discord
            </a>
          </div>
          <div class="separator hidden md:block" />
          <div>
            <h1 class="login-title">
              No Discord?
            </h1>
            <p class="login-description text-gray-400 mb-4">
              Go ahead then and enter your Altify account credentials
            </p>
            <form action="" method="post">
              <div v-if="incorrect" class="incorrect-label">
                These credentials don't match any account
              </div>
              <input type="text" :class="{'login-input' : true, 'incorrect' : incorrect}" placeholder="Enter email or username" required>
              <input type="password" placeholder="Enter your password" :class="{'mb-6 login-input' : true, 'incorrect' : incorrect}" required>
              <div class="flex justify-start items-center mb-6">
                <label class="checkmark-container">
                  <p class="font-light">Remember me</p>
                  <input type="checkbox">
                  <span class="checkmark" />
                </label>
              </div>
              <a class="btn btn-secondary" href="#" target="_blank">
                Log in
              </a>
            </form>
            <div class="mt-6">
              <NuxtLink to="/forgotten-password" class="nav-link block md:inline-block">
                Forgot your password?
              </NuxtLink>
              <NuxtLink to="/register" class="nav-link block md:inline-block">
                No account yet?
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
  name: 'LoginPage',
  data () {
    return {
      incorrect: false
    }
  }
}
</script>

<style>
</style>
