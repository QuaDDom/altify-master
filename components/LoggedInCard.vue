<template>
  <div class="hidden relative md:flex justify-center items-center text-white text-xl">
    <NuxtLink to="/cart" class="block mr-8">
      <font-awesome-icon icon="fa-solid fa-shopping-cart" />
      <div class="cart-badge">
        1
      </div>
    </NuxtLink>
    <div class="flex justify-center items-center  login-card h-full">
      <div class="flex justify-center items-center cursor-pointer">
        <img src="https://picsum.photos/200" alt="User avatar" class="navbar-pfp">
        <span>GoodGuyGopes</span>
        <font-awesome-icon icon="fa-solid fa-caret-down" class="ml-2" />
      </div>
      <div class="user-dropdown-wrapper">
        <div class="user-dropdown">
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

<style scoped>

</style>
