<template>
  <div>
    <div class="div-centering full-size px-5 my-5 md:my-0">
      <div>
        <AltifyLogo />
        <div class="md:div-centering">
          <div>
            <h1 class="login-title">
              Set up a new password
            </h1>
            <form action="" method="post">
              <input type="password" :class="{'login-input' : true}" placeholder="Enter new password" required>
              <input type="password" :class="{'login-input mb-6' : true}" placeholder="Confirm new password" required>
              <a class="btn btn-secondary" href="#" target="_blank">
                Change password
              </a>
            </form>
            <p class="login-description text-gray-400 mt-4">
              After successfully changing your password, you will be redirected to the login page.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NewPasswordPage',
  data () {
    return {
      sent: false
    }
  }
}
</script>

<style>
</style>
