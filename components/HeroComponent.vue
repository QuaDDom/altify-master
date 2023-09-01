<template>
  <div class="hero">
    <div class="container mx-auto px-8 mb-32 grid grid-cols-1 gap-x-16 md:grid-cols-2">
      <div>
        <h1 id="title">
          Introducing Altify
        </h1>
        <p>
          At Altify, we not only provide you various services cheaper than anywhere else, we also sell methods that we use, so you can either buy everything yourself or open a service of your own!
        </p>
        <div class="mt-6">
          <a class="btn btn-primary mr-3 mb-2" href="#scroll-services">
            Our services
          </a>
          <a class="btn btn-secondary" href="https://discord.gg/altify" target="_blank">
            Discord
          </a>
        </div>
      </div>
      <div class="md:flex justify-center items-center hidden">
        <img src="../assets/img/planetyellow.png" class="planet p-yellow">
        <img src="../assets/img/planetpurple.png" class="planet p-purple">
        <img src="../assets/img/player.png" class="img-player">
      </div>
    </div>
    <div id="scroll-services" class="flex justify-center items-center font-medium text-gray-200 text-xl">
      <div class="characteristic">
        <font-awesome-icon icon="fa-solid fa-check" class="blue-check" />
        <span>Fast service</span>
      </div>
      <div class="characteristic">
        <font-awesome-icon icon="fa-solid fa-check" class="blue-check" />
        <span>Cheap prices</span>
      </div>
      <div class="characteristic">
        <font-awesome-icon icon="fa-solid fa-check" class="blue-check" />
        <span>24/7 support</span>
      </div>
    </div>
  </div>
</template>

<style>
.characteristic {
  @apply m-2 flex justify-center items-center;
  font-family: 'Montserrat';
}
.blue-check {
  @apply mr-2;
  color: #007bd2;
}
.hero {
  background: url('../assets/img/background.png');
  background-position: top center;
  background-size: cover;
  @apply pt-40 md:pt-72 pb-32;
}
.img-player {
  width: 300px;
  animation: movement-player 6s infinite linear;
  animation-delay: 2s;
}
.p-purple {
  margin-left: -300px;
  margin-top: -300px;
  animation: movement-purple 21s infinite linear;
}
.p-yellow {
  margin-right: -250px;
  margin-top: -200px;
  animation: movement-yellow 14s infinite linear;
  animation-delay: 1s;
}
.planet {
  position: absolute;
}
#title {
  @apply mb-4;
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 700;
  font-size: 48px;

  color: #FFFFFF;
}
p {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 300;
  font-size: 20px;
  line-height: 23px;
  display: flex;
  align-items: center;
  color: #D5D5D5;
}
.nuxt-logo {
  height: 180px;
}

@keyframes movement-yellow {
  0%   {transform: translateY(-10px) translateX(0) rotate(0);}
  25%  {transform: translateY(10px) translateX(0px) rotate(90deg);}
  50%  {transform: translateY(-10px) translateX(0) rotate(180deg);}
  75%   {transform: translateY(10px) translateX(0) rotate(270deg);}
  100%   {transform: translateY(-10px) translateX(0) rotate(360deg);}
}

@keyframes movement-purple {
  0%   {transform: translateY(0px) translateX(0) rotate(0deg);}
  50%  {transform: translateY(30px) translateX(0px) rotate(20deg);}
  100%  {transform: translateY(0px) translateX(0) rotate(0deg);}
}

@keyframes movement-player {
  0%   {transform: translateY(0px) translateX(0);}
  50%  {transform: translateY(10px) translateX(0px);}
  100%  {transform: translateY(0px) translateX(0);}
}

</style>
