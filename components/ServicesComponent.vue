<template>
  <div id="services" class="text-center" @mousemove="mouseMove">
    <div class="flex justify-center my-24">
      <h1 class="services-background">
        Services
      </h1>
      <h1 class="services-title">
        Services
      </h1>
    </div>
    <div class="cards mb-20">
      <span class="category-title">
        Spotify services
      </span>
      <div v-for="[key, service] in Object.entries(spotify)" :key="'spotify-' + key" :ref="'spotify-' + key" class="item-wrapper" style="">
        <div class="item-content">
          <div>
            <span class="service-type">
              {{ service.type }}
            </span>
            <span class="service-name">
              {{ service.name }}
            </span>
            <span class="service-duration">
              {{ service.duration }}
            </span>
            <span class="service-price">
              {{ service.price }}
            </span>
            <button class="service-buy">
              Add to cart
            </button>
          </div>
        </div>
      </div>
      <span class="category-title">
        Discord services
      </span>
      <div v-for="[key, service] in Object.entries(discord)" :key="'discord-' + key" :ref="'discord-' + key" class="item-wrapper" style="">
        <div class="item-content">
          <div>
            <span class="service-type">
              {{ service.type }}
            </span>
            <span class="service-name">
              {{ service.name }}
            </span>
            <span class="service-duration">
              {{ service.duration }}
            </span>
            <span class="service-price">
              {{ service.price }}
            </span>
            <button class="service-buy">
              Add to cart
            </button>
          </div>
        </div>
      </div>
      <span class="category-title">
        Twitch services
      </span>
      <div v-for="[key, service] in Object.entries(twitch)" :key="'twitch-' + key" :ref="'twitch-' + key" class="item-wrapper" style="">
        <div class="item-content">
          <div>
            <span class="service-type">
              {{ service.type }}
            </span>
            <span class="service-name">
              {{ service.name }}
            </span>
            <span class="service-duration">
              {{ service.duration }}
            </span>
            <span class="service-price">
              {{ service.price }}
            </span>
            <button class="service-buy">
              Add to cart
            </button>
          </div>
        </div>
      </div>
      <span class="category-title">
        Instagram services
      </span>
      <div v-for="[key, service] in Object.entries(instagram)" :key="'instagram-' + key" :ref="'instagram-' + key" class="item-wrapper" style="">
        <div class="item-content">
          <div>
            <span class="service-type">
              {{ service.type }}
            </span>
            <span class="service-name">
              {{ service.name }}
            </span>
            <span class="service-duration">
              {{ service.duration }}
            </span>
            <span class="service-price">
              {{ service.price }}
            </span>
            <button class="service-buy">
              Add to cart
            </button>
          </div>
        </div>
      </div>
    </div>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#0b0d0f" fill-opacity="1" d="M0,96L0,64L51.4,64L51.4,160L102.9,160L102.9,192L154.3,192L154.3,96L205.7,96L205.7,96L257.1,96L257.1,0L308.6,0L308.6,96L360,96L360,224L411.4,224L411.4,64L462.9,64L462.9,160L514.3,160L514.3,256L565.7,256L565.7,128L617.1,128L617.1,288L668.6,288L668.6,160L720,160L720,256L771.4,256L771.4,288L822.9,288L822.9,96L874.3,96L874.3,160L925.7,160L925.7,192L977.1,192L977.1,160L1028.6,160L1028.6,64L1080,64L1080,64L1131.4,64L1131.4,96L1182.9,96L1182.9,64L1234.3,64L1234.3,192L1285.7,192L1285.7,160L1337.1,160L1337.1,192L1388.6,192L1388.6,96L1440,96L1440,320L1388.6,320L1388.6,320L1337.1,320L1337.1,320L1285.7,320L1285.7,320L1234.3,320L1234.3,320L1182.9,320L1182.9,320L1131.4,320L1131.4,320L1080,320L1080,320L1028.6,320L1028.6,320L977.1,320L977.1,320L925.7,320L925.7,320L874.3,320L874.3,320L822.9,320L822.9,320L771.4,320L771.4,320L720,320L720,320L668.6,320L668.6,320L617.1,320L617.1,320L565.7,320L565.7,320L514.3,320L514.3,320L462.9,320L462.9,320L411.4,320L411.4,320L360,320L360,320L308.6,320L308.6,320L257.1,320L257.1,320L205.7,320L205.7,320L154.3,320L154.3,320L102.9,320L102.9,320L51.4,320L51.4,320L0,320L0,320Z" /></svg>
    <div class="footer-bg text-center pb-28">
      <h1 class="footer-title">
        Can't get enough?
      </h1>
      <span class="footer-desc inline-block mx-2">
        Check out our very own method - unlimited turkish VCCs, unlimited turkish discounts! Never seen before, leak-proof!
      </span>
      <div class="container mx-auto lg:px-48 mt-10">
        <div v-for="[key, method] in Object.entries(methods)" :key="'method-' + key">
          <div :ref="'method-' + key" class="method-wrapper" style="" @click="expand_faq(key)">
            <div class="method-content py-3 lg:grid lg:grid-cols-2 justify-between">
              <div class="text-center lg:text-left flex items-center justify-center lg:justify-start px-9 pt-5 lg:pt-0">
                <div>
                  <span class="method-type">
                    Method
                  </span>
                  <span class="method-name">
                    {{ method.name }}
                  </span>
                  <span class="method-duration">
                    one-time payment
                  </span>
                </div>
              </div>
              <div class="flex items-center justify-center lg:justify-end lg:px-9">
                <div class="py-1">
                  <span class="method-price">
                    {{ method.price }}
                  </span>
                  <!--button class="btn-small btn-dark mt-2">
                    Expand
                  </button-->
                </div>
                <font-awesome-icon icon="fa-solid fa-arrow-down" :class="{'ml-4 text-gray-500 text-2xl arrow-still' : true, 'arrow-rotate' : methods[key].expand}" />
              </div>
            </div>
          </div>
          <div :class="{'method-faq-wrapper' : true, 'method-expanded' : methods[key].expand}">
            <div v-for="[qk, q] in Object.entries(methods_faq[key])" :key="'method-' + key + '-' + qk">
              <div class="method-faq mt-3">
                <div class="method-faq-content">
                  {{ q.question }}
                  <button class="btn-small btn-dark ml-auto" @click="expand_question(key, qk)">
                    <span v-if="!methods_faq[key][qk].expand ">
                      Expand
                    </span>
                    <span v-else>
                      Collapse
                    </span>
                  </button>
                </div>
              </div>
              <div :class="{'method-faq mt-2' : true, 'hidden' : !methods_faq[key][qk].expand }">
                <!-- eslint-disable-next-line vue/multiline-html-element-content-newline -->
                <div class="method-faq-content break-lines">{{ q.answer }}
                </div>
              </div>
            </div>
            <button class="btn btn-blue mt-3">
              Add {{ method.name }} to cart
              <font-awesome-icon icon="fa-solid fa-arrow-right" class="ml-2" />
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      mouse: {
        x: 0,
        y: 0
      },
      spotify: [
        {
          type: 'Spotify',
          name: 'Premium Duo',
          duration: 'monthly',
          price: '3.5€'
        },
        {
          type: 'Spotify',
          name: 'Individual',
          duration: 'monthly',
          price: '2.25€'
        },
        {
          type: 'Spotify',
          name: 'Dedicated Family',
          duration: 'monthly',
          price: '4.5€'
        }
      ],
      discord: [
        {
          type: 'Discord',
          name: 'Nitro Basic',
          duration: 'monthly',
          price: '2€'
        },
        {
          type: 'Discord',
          name: 'Nitro Basic',
          duration: 'yearly',
          price: '12€'
        },
        {
          type: 'Discord',
          name: 'Nitro Boost',
          duration: 'monthly',
          price: '3.5€'
        },
        {
          type: 'Discord',
          name: 'Nitro Boost',
          duration: 'yearly',
          price: '20€'
        }
      ],
      twitch: [
        {
          type: 'Twitch',
          name: 'Tier 1',
          duration: 'monthly',
          price: '1.5€'
        },
        {
          type: 'Twitch',
          name: 'Tier 2',
          duration: 'monthly',
          price: '2€'
        },
        {
          type: 'Twitch',
          name: 'Tier 3',
          duration: 'monthly',
          price: '3.5€'
        }
      ],
      instagram: [
        {
          type: 'Instagram',
          name: 'Followers',
          duration: 'per 1000',
          price: '0.4€'
        },
        {
          type: 'Instagram',
          name: 'Likes',
          duration: 'per 1000',
          price: '0.2€'
        }
      ],
      methods: [
        {
          name: 'Turkey VCC method',
          price: '35€',
          expand: false
        },
        {
          name: 'Robux method',
          price: '15€',
          expand: false
        }
      ],
      methods_faq: [
        [
          {
            question: 'So, how does it work?',
            answer: 'You will be asked to download 2 apps.\n\nTop-up app - this will be used just for topping up the VCC itself. You are required to provide 18+ ID, however the country doesn\'t have to be Turkish. Any attempts to commit fraud/identity theft are not our responsibility, Altify never encourages you to use ID you don\'t have permission to use.\n\nVCC app - this app will be used for generating said Turkish VCCs. You don\'t need anything - you will be given phone number to verify with and basically anything required for the app to work.',
            expand: false
          },
          {
            question: 'Are there any known limitations?',
            answer: 'There are 3 limitations:\n1. 120$ monthly top-up limit.\n2. maximum 3 VCCs generated per year.\n3. steam region change doesn\'t work (but after region change, buying games works just fine)' +
            '\n\nThese limits are not bypassable, however included in the method price is a guarantee we will help you with making new accounts when you run out. Be advised we reserve the right to ask for proof of having at least one of the limits fullfilled. These rules are essential to prevent the method from being leaked which would lead to you losing money.',
            expand: false
          },
          {
            question: 'Is this the Oldubil/google/apple method?',
            answer: 'No! This method is completely proprietary and we guarantee you it is not leaked nor will it ever be thanks to our security measures in place!',
            expand: false
          },
          {
            question: 'How do the top-ups work?',
            answer: 'The top-ups are instant, so there is no more waiting for days. As for fees, we did our best to find a way to minimalize them as much as possible.',
            expand: false
          },
          {
            question: 'I am underage and my parents don\'t allow me to use their ID, what should I do?',
            answer: 'In that case, we can offer to do the top-ups for you, for a fee: 3% + 0,5€, with a minimum fee of 2€. Sadly, there is no other way to do this.',
            expand: false
          },
          {
            question: 'I am from the U.S., will it work for me?',
            answer: 'From our experience, people from the U.S. have trouble topping up the VCC. For now, there is no workaround (our last one got patched), so the only thing we can do is offer you top-ups (see above).',
            expand: false
          }
        ],
        [
          {
            question: 'How many times can I use this method?',
            answer: 'The method can be used as many times as you want, and we can find you a deal for any amount you want.',
            expand: false
          },
          {
            question: 'What do I need to use this method?',
            answer: 'You need Premium and small limited (~ 80 robux)',
            expand: false
          },
          {
            question: 'Is this method safe?',
            answer: 'Yes, it is safe. We check the poisoned limites so you\'re dealing with clean robux.',
            expand: false
          }
        ]
      ]
    }
  },
  methods: {
    expand_faq (id) {
      this.methods[id].expand = !this.methods[id].expand
    },
    expand_question (key, id) {
      this.methods_faq[key][id].expand = !this.methods_faq[key][id].expand
    },
    mouseMove (event) {
      // eslint-disable-next-line no-unused-vars
      for (let key = 0; key < this.spotify.length; key++) {
        const object = this.$refs['spotify-' + key][0]
        object.style.setProperty('--mouse-x', event.pageX - object.offsetLeft + 'px')
        object.style.setProperty('--mouse-y', event.pageY - object.offsetTop + 'px')
      }
      for (let key = 0; key < this.discord.length; key++) {
        const object = this.$refs['discord-' + key][0]
        object.style.setProperty('--mouse-x', event.pageX - object.offsetLeft + 'px')
        object.style.setProperty('--mouse-y', event.pageY - object.offsetTop + 'px')
      }
      for (let key = 0; key < this.twitch.length; key++) {
        const object = this.$refs['twitch-' + key][0]
        object.style.setProperty('--mouse-x', event.pageX - object.offsetLeft + 'px')
        object.style.setProperty('--mouse-y', event.pageY - object.offsetTop + 'px')
      }
      for (let key = 0; key < this.instagram.length; key++) {
        const object = this.$refs['instagram-' + key][0]
        object.style.setProperty('--mouse-x', event.pageX - object.offsetLeft + 'px')
        object.style.setProperty('--mouse-y', event.pageY - object.offsetTop + 'px')
      }
      for (let key = 0; key < this.methods.length; key++) {
        const object = this.$refs['method-' + key][0]
        object.style.setProperty('--mouse-x', event.pageX - object.offsetLeft + 'px')
        object.style.setProperty('--mouse-y', event.pageY - object.offsetTop + 'px')
      }
    }
  }
}
</script>

<style>
.category-title {
  display: block;
  color: #58747E;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  display: block;
  margin-bottom: 10px;
  margin-top: 25px;
}

.service-type {
  background: linear-gradient(264.31deg, #00A1FB 0%, #0064FB 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-fill-color: transparent;

  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  display: block;
}
.service-name {
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  color: #D9D9D9;
  display: block;
}
.service-duration {
  color: #58747E;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  display: block;
}
.service-price {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  color: #D9D9D9;
  display: block;
  padding-top: 10px;
}
.service-buy {
  background: linear-gradient(92.24deg, #00A0FB 0%, #0064FB 100%);
  border-radius: 10px;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  color: #FFFFFF;
  @apply px-7 py-1 mt-2;
  border-radius: 30px;
  z-index: 100;
  position: relative;
  cursor: pointer;
}
.services-title {
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  z-index: 1;

  color: #FFFFFF;
}
.services-background {
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 700;
  color: #131619;
  font-size: 130px;
  margin-top: -70px;
  position: absolute;

  @apply hidden sm:block;

  text-shadow: -1px 0 #007bd2, 0 1px #007bd2, 1px 0 #007bd2, 0 -1px #007bd2;
}

/* Item Cards */
.cards {
  @apply container mx-auto xl:px-32 px-0;
}

:root {
  --bg-color: #353b45;
  --content-color: #15191c;
  --method-content-color: #0d1013;
}

.item-wrapper {
  cursor: pointer;
  vertical-align:top;
  margin: 8px;
  height: 250px;
  width: 250px;
  display: inline-block;
  background: var(--bg-color);
  border-radius: 15px;
  position: relative;
}

.item-wrapper::after {
  background: radial-gradient(
    800px circle at var(--mouse-x) var(--mouse-y),
    rgba(255, 255, 255, 0.5),
    transparent 40%
  );
  z-index: 1;
}

.item-wrapper > .item-content {
  margin: 1px;
  height: calc(100% - 2px);
  width: calc(100% - 2px);
  background-color: var(--content-color);
  border-radius: inherit;
  z-index: 2;
  position: relative;
  display: flex;
  @apply justify-center items-center;
}
.item-wrapper::before, .item-wrapper::after {
  border-radius: inherit;
  content: '';
  height: 100%;
  left: 0px;
  position: absolute;
  top: 0px;
  width: 100%;
  transition: opacity .5s;
}
.item-wrapper::after {
  z-index: 1;
}

.item-wrapper::before {
  background: radial-gradient(
    800px circle at var(--mouse-x) var(--mouse-y),
    rgba(255, 255, 255, 0.06), transparent 40%
  );
  opacity: 0;
  z-index: 3;
}

.item-wrapper:hover::before {
  opacity: 1;
}

/* Method */
.method-wrapper {
  cursor: pointer;
  vertical-align:top;
  width: 90%;
  max-width: 1048px;
  display: inline-block;
  background: var(--bg-color);
  border-radius: 15px;
  position: relative;
  @apply mt-5;
}

.method-wrapper::after {
  background: radial-gradient(
    600px circle at var(--mouse-x) var(--mouse-y),
    rgba(255, 255, 255, 0.4),
    transparent 40%
  );
  z-index: 1;
}

.method-wrapper > .method-content {
  margin: 1px;
  height: calc(100% - 2px);
  width: calc(100% - 2px);
  background-color: var(--method-content-color);
  border-radius: inherit;
  z-index: 2;
  position: relative;
}
.method-wrapper::before, .method-wrapper::after {
  border-radius: inherit;
  content: '';
  height: 100%;
  left: 0px;
  position: absolute;
  top: 0px;
  width: 100%;
  transition: opacity .5s;
}
.method-wrapper::after {
  z-index: 1;
}

.method-wrapper::before {
  background: radial-gradient(
    600px circle at var(--mouse-x) var(--mouse-y),
    rgba(131, 150, 207, 0.04), transparent 40%
  );
  opacity: 0;
  z-index: 3;
}

.method-wrapper:hover::before {
  opacity: 1;
}

.method-type {
  background: linear-gradient(264.31deg, #00A1FB 0%, #0064FB 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-fill-color: transparent;

  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  display: block;
}
.method-name {
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 700;
  font-size: 30px;
  color: #D9D9D9;
  display: block;
}
.method-duration {
  color: #58747E;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  display: block;
}
.method-price {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 72px;
  display: block;
  background: linear-gradient(47.54deg, #00BFFB 13.27%, #0047B1 85.59%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-fill-color: transparent;
  line-height: 72px;
}
</style>
