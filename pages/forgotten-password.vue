<template>
  <div>
    <div class="div-centering full-size px-5 my-5 md:my-0">
      <div>
        <AltifyLogo />
        <div class="md:div-centering">
          <div>
            <h1 class="login-title">
              Recover your password
            </h1>
            <form action="" method="post">
              <p class="login-description text-gray-400 mb-4">
                Enter your email and if it is found in our database, we will send you a link to recover your password.
              </p>
              <div v-if="sent" class="correct-label">
                Email sent!
              </div>
              <input type="email" :class="{'login-input mb-6' : true}" placeholder="Enter your email" required>
              <a class="btn btn-secondary" href="#" target="_blank">
                Send recovery email
              </a>
            </form>
            <div class="mt-6">
              <NuxtLink to="/login" class="nav-link block md:inline-block">
                {{ '<' }} Go back
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
  name: 'ForgottenPasswordPage',
  data () {
    return {
      sent: false
    }
  }
}
</script>

<style>
</style>
