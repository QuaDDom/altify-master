<template>
  <div>
    <div class="pt-20 pb-20 px-5 my-5 md:my-0">
      <div>
        <AltifyLogo />
        <div class="md:div-centering">
          <div>
            <h1 class="login-title">
              Choose payment method
            </h1>
            <div>
              <button class="cart-item cart-payment w-full">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-brands fa-paypal'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-name">
                      Paypal
                    </span>
                  </div>
                </div>
              </button>
              <button class="cart-item cart-payment w-full">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-brands fa-bitcoin'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-name">
                      Crypto
                    </span>
                  </div>
                </div>
              </button>
              <button class="cart-item cart-payment w-full">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-solid fa-dollar-sign'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-name">
                      CashApp
                    </span>
                  </div>
                </div>
              </button>
              <button class="cart-item cart-payment w-full">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-solid fa-building-columns'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-name">
                      Bank Transfer
                    </span>
                  </div>
                </div>
              </button>
              <button class="cart-item cart-payment w-full">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-solid fa-r'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-name">
                      Revolut
                    </span>
                  </div>
                </div>
              </button>
              <button class="cart-item cart-payment w-full">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-solid fa-flag'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-name">
                      Wise
                    </span>
                  </div>
                </div>
              </button>
              <button class="cart-item cart-payment w-full">
                <div class="flex items-center justify-start">
                  <font-awesome-icon
                    :icon="'fa-solid fa-credit-card'"
                    class="mr-5 text-3xl text-gray-400"
                  />
                  <div>
                    <span class="service-name">
                      Card
                    </span>
                  </div>
                </div>
              </button>
            </div>
            <div class="">
              <div class="text-center">
                <NuxtLink class="btn btn-secondary" to="/cart">
                  Back
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
  name: 'PaymentPage',
  data () {
    return {
      sent: false
    }
  }
}
</script>

<style>
</style>
