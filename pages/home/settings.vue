<template>
  <div>
    <div class="div-centering md:h-screen px-5 my-5 md:my-0">
      <div>
        <NuxtLink to="/home" class="nav-link block text-center mb-4">
          <font-awesome-icon icon="fa-solid fa-arrow-left" />
          Back
        </NuxtLink>
        <AltifyLogo />
        <div class="md:div-centering">
          <div>
            <h1 class="login-title">
              Settings
            </h1>
            <form action="" method="post">
              <div v-if="email" class="incorrect-label">
                This email address is already taken!
              </div>
              <div v-if="username" class="incorrect-label">
                This username is already taken!
              </div>
              <div v-if="password" class="incorrect-label">
                Entered passwords don't match!
              </div>
              <input type="text" :class="{'login-input' : true, 'incorrect' : username}" placeholder="Username" required>
              <input type="text" :class="{'login-input' : true, 'incorrect' : email}" placeholder="Email" required>
              <input type="password" placeholder="Enter your old password" :class="{'login-input' : true, 'incorrect' : password}" required>
              <input type="password" placeholder="Enter new password" :class="{'mb-6 login-input' : true, 'incorrect' : password}" required>
              <a class="btn btn-secondary" href="#" target="_blank">
                Save settings
              </a>
            </form>
          </div>
          <div class="ml-12 separator hidden md:block" />
          <div class="my-6">
            <h1 class="login-title">
              Discord account
            </h1>
            <p class="login-description text-gray-400 mb-4">
              Use Discord for quick authentication and identification on our Discord server!
            </p>
            <a v-if="false" class="btn btn-blue" href="#" target="_blank">
              Connect your Discord account
            </a>
            <div v-else class="discord-wrapper">
              <div class="flex justify-start items-center">
                <img src="https://picsum.photos/200" alt="User avatar" class="navbar-pfp">
                <div class="discord-details">
                  <p>GoodGuyGopes</p>
                  <span>#3518</span>
                </div>
              </div>
              <button class="discord-disconnect">
                <font-awesome-icon icon="fa-solid fa-link-slash" />
              </button>
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
      username: false,
      email: false,
      password: false
    }
  }
}
</script>

<style>
</style>
