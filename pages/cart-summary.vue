<template>
  <div>
    <div class="pt-20 pb-20 px-5 my-5 md:my-0">
      <div>
        <AltifyLogo />
        <div class="md:div-centering">
          <div>
            <h1 class="login-title">
              Summary
            </h1>
            <div>
              <div v-for="i in 3" :key="i" class="my-4">
                <div class="flex items-center">
                  <span class="service-duration mr-5">
                    1x
                  </span>
                  <span class="service-type inline-block mr-2">
                    Twitter
                  </span>
                  <span class="cart-category">
                    1000 follower
                  </span>
                  <span class="ml-auto cart-category font-bold">
                    2.5 e
                  </span>
                </div>
                <div class="pl-4 mt-3 grid grid-cols-2">
                  <div>
                    <span class="category-details">
                      Profile link
                    </span>
                  </div>
                  <div class="text-right">
                    <span class="category-details">
                      https://music.youtube.com/watch?v=tmvk96p4Iaw&list=OLAK5uy_kd6PGi4CZLx4_kHztpKd7Rht-XrCTpmS4
                    </span>
                  </div>
                </div>
              </div>
            </div>
            <hr>
            <div class="my-6 flex">
              <span class="cart-price">
                Total:
              </span>
              <span class="cart-price ml-auto">
                5 €
              </span>
            </div>
            <div class="md:grid md:grid-cols-2 mt-2">
              <div class="text-left" />
              <div class="mt-3 md:mt-0 md:text-right">
                <NuxtLink class="btn btn-blue" to="/payment">
                  Complete order
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CartPage',
  data () {
    return {
      sent: false
    }
  }
}
</script>

<style>
</style>
