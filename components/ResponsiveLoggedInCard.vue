<template>
  <div>
    <div v-if="false">
      <div class="text-center">
        <NuxtLink to="/login" class="btn btn-primary mr-3 mb-2" href="#scroll-services">
          Log in
        </NuxtLink>
      </div>
      <div class="text-center">
        <NuxtLink to="/register" class="btn btn-secondary mr-3 mb-2" href="#scroll-services">
          Sign up
        </NuxtLink>
      </div>
    </div>
    <div v-else class="relative flex justify-center items-center text-white text-xl">
      <div class="login-card h-full">
        <div class="flex justify-center items-center cursor-pointer">
          <img src="https://picsum.photos/200" alt="User avatar" class="navbar-pfp">
          <span>GoodGuyGopes</span>
        </div>
        <div class="user-dropdown mt-3">
          <NuxtLink to="/home">
            <font-awesome-icon icon="fa-solid fa-envelopes-bulk" class="mr-2" />
            Tickets
          </NuxtLink>
          <NuxtLink to="/home/settings">
            <font-awesome-icon icon="fa-solid fa-cogs" class="mr-2" />
            Settings
          </NuxtLink>
          <NuxtLink to="#" class="logout-hover">
            <font-awesome-icon icon="fa-solid fa-right-from-bracket" class="mr-2" />
            Logout
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>
