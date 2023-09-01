<template>
  <div>
    <div class="pt-20 pb-20 px-5 my-5 md:my-0">
      <div>
        <AltifyLogo />
        <div class="md:div-centering">
          <div>
            <h1 class="login-title">
              Your shopping cart
            </h1>
            <div>
              <div class="cart-item">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-brands fa-instagram'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-type">
                      Instagram
                    </span>
                    <span class="service-name">
                      1000 Followers
                    </span>
                    <span class="service-duration">
                      one-time purchase
                    </span>
                  </div>
                </div>
                <div class="flex items-center justify-end">
                  <div class="text-right">
                    <span class="cart-price mx-2">
                      2.50 €
                    </span>
                    <div class="flex items-center justify-end">
                      <span class="service-duration">Quantity:</span>
                      <input type="number" min="1" value="1" class="quantity-input">
                      <a href="#" class="cart-remove">Remove</a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="cart-item">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-brands fa-instagram'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-type">
                      Instagram
                    </span>
                    <span class="service-name">
                      1000 Followers
                    </span>
                    <span class="service-duration">
                      one-time purchase
                    </span>
                  </div>
                </div>
                <div class="flex items-center justify-end">
                  <div class="text-right">
                    <span class="cart-price mx-2">
                      2.50 €
                    </span>
                    <div class="flex items-center justify-end">
                      <span class="service-duration">Quantity:</span>
                      <input type="number" min="1" value="1" class="quantity-input">
                      <a href="#" class="cart-remove">Remove</a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="cart-item">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-brands fa-instagram'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-type">
                      Instagram
                    </span>
                    <span class="service-name">
                      1000 Followers
                    </span>
                    <span class="service-duration">
                      one-time purchase
                    </span>
                  </div>
                </div>
                <div class="flex items-center justify-end">
                  <div class="text-right">
                    <span class="cart-price mx-2">
                      2.50 €
                    </span>
                    <div class="flex items-center justify-end">
                      <span class="service-duration">Quantity:</span>
                      <input type="number" min="1" value="1" class="quantity-input">
                      <a href="#" class="cart-remove">Remove</a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="cart-item">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-brands fa-instagram'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-type">
                      Instagram
                    </span>
                    <span class="service-name">
                      1000 Followers
                    </span>
                    <span class="service-duration">
                      one-time purchase
                    </span>
                  </div>
                </div>
                <div class="flex items-center justify-end">
                  <div class="text-right">
                    <span class="cart-price mx-2">
                      2.50 €
                    </span>
                    <div class="flex items-center justify-end">
                      <span class="service-duration">Quantity:</span>
                      <input type="number" min="1" value="1" class="quantity-input">
                      <a href="#" class="cart-remove">Remove</a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="cart-item">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-brands fa-instagram'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-type">
                      Instagram
                    </span>
                    <span class="service-name">
                      1000 Followers
                    </span>
                    <span class="service-duration">
                      one-time purchase
                    </span>
                  </div>
                </div>
                <div class="flex items-center justify-end">
                  <div class="text-right">
                    <span class="cart-price mx-2">
                      2.50 €
                    </span>
                    <div class="flex items-center justify-end">
                      <span class="service-duration">Quantity:</span>
                      <input type="number" min="1" value="1" class="quantity-input">
                      <a href="#" class="cart-remove">Remove</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="my-6 flex">
              <span class="cart-price">
                Total:
              </span>
              <span class="cart-price ml-auto">
                5 €
              </span>
            </div>
            <div class="md:grid md:grid-cols-2">
              <div class="text-left">
                <NuxtLink class="btn btn-secondary" to="/">
                  Continue shopping
                </NuxtLink>
              </div>
              <div class="mt-3 md:mt-0 md:text-right">
                <NuxtLink class="btn btn-blue" to="/cart-details">
                  Checkout
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
