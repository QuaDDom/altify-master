<template>
  <div id="footer" class="">
    <div class="min-footer lg:grid lg:grid-cols-3 px-16 py-4 footer-darker">
      <div class="py-2 lg:py-0 flex justify-center lg:jutify-start items-center">
        <img src="../assets/img/logo.png" class="logo-footer">
        <span class="logo-text">Altify</span>
      </div>
      <div class="flex justify-center items-center py-2 lg:py-0">
        <a href="https://marweb.eu/" target="_blank" class="signature">Designed by marweb.eu</a>
      </div>
      <div class="py-2 lg:py-0 text-white text-xl flex justify-center lg:jutify-end items-center">
        <a href="mailto:info@altify.store" target="_blank">
          <font-awesome-icon icon="fa-solid fa-envelope" class="mx-2" />
        </a>
        <a href="https://www.instagram.com/altifyshop/" target="_blank">
          <font-awesome-icon icon="fa-brands fa-instagram" class="mx-2" />
        </a>
        <a href="https://discord.gg/altify" target="_blank">
          <font-awesome-icon icon="fa-brands fa-discord" class="mx-2" />
        </a>
        <a href="https://www.tiktok.com/@altify.store" target="_blank">
          <font-awesome-icon icon="fa-brands fa-tiktok" class="mx-2" />
        </a>
      </div>
    </div>
  </div>
</template>

<style>
.footer-darker {
  background-color: #090b0d;
}
.signature {
  font-family: 'Montserrat';
  color: #75919c;
}
.logo-footer {
  width: 50px;
}
.footer-bg {
  background-color: #0b0d0f;
  margin-top: -1px;
}
.footer-title {
  @apply pt-12;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 48px;

  color: #FFFFFF;
}
.footer-desc {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 300;
  font-size: 18px;
  line-height: 23px;
  align-items: center;
  color: #D5D5D5;
  max-width: 500px;
}
</style>
