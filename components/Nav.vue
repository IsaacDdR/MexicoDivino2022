<template>
  <div
    class="px-4 py-5 mx-auto sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8"
  >
    <div class="relative flex grid items-center grid-cols-2 lg:grid-cols-3">
      <ul class="flex items-center hidden space-x-8 lg:flex">
        <li>
          <NuxtLink
            to="/"
            aria-label="Blog"
            title="Blog"
            class="font-medium tracking-wide text-gray-700 transition-colors duration-200"
            >Blog</NuxtLink
          >
        </li>
        <li>
          <NuxtLink
            to="/"
            aria-label="Servicios"
            title="Servicios"
            class="font-medium tracking-wide text-gray-700 transition-colors duration-200"
            >Servicios</NuxtLink
          >
        </li>
      </ul>
      <NuxtLink
        to="/"
        aria-label="Cintatic"
        title="Cintatic"
        class="inline-flex items-center lg:mx-auto"
      >
        <nuxt-img class="w-24" src="/icon.png" />
      </NuxtLink>
      <ul class="flex items-center hidden ml-auto space-x-8 lg:flex">
        <li class="">
          <a href="https://instagram.com/cintaticmx">
            <nuxt-img
              class="inline-block align-middle ml-3 text-3xl w-8"
              src="/icons/instagram-brands.svg"
            />
          </a>

          <a href="https://facebook.com/cintaticmx">
            <nuxt-img
              class="inline-block align-middle ml-3 text-3xl w-8"
              src="/icons/facebook-brands.svg"
            />
          </a>
          <a
            href="https://api.whatsapp.com/send?phone=525628348062&text=%C2%A1Hola!%20Quisiera%20saber%20m%C3%A1s%20informaci%C3%B3n%20acerca%20de%20sus%20servicios."
          >
            <nuxt-img
              src="/icons/whatsapp-brands.svg"
              class="inline-block align-middle ml-3 w-8"
            />
          </a>
        </li>
        <li></li>
      </ul>
      <div class="ml-auto lg:hidden">
        <button
          aria-label="Open Menu"
          title="Open Menu"
          class="p-2 -mr-1 transition duration-200 rounded focus:outline-none focus:shadow-outline"
          @click="isMenuOpen = !isMenuOpen"
        >
          <svg class="w-5 text-gray-600" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M23,13H1c-0.6,0-1-0.4-1-1s0.4-1,1-1h22c0.6,0,1,0.4,1,1S23.6,13,23,13z"
            ></path>
            <path
              fill="currentColor"
              d="M23,6H1C0.4,6,0,5.6,0,5s0.4-1,1-1h22c0.6,0,1,0.4,1,1S23.6,6,23,6z"
            ></path>
            <path
              fill="currentColor"
              d="M23,20H1c-0.6,0-1-0.4-1-1s0.4-1,1-1h22c0.6,0,1,0.4,1,1S23.6,20,23,20z"
            ></path>
          </svg>
        </button>
        <div v-if="isMenuOpen" class="z-50 absolute top-0 left-0 w-full">
          <div class="p-5 bg-white border rounded shadow-sm">
            <div class="flex items-center justify-between mb-4">
              <div>
                <NuxtLink
                  to="/"
                  aria-label="Company"
                  title="Company"
                  class="inline-flex items-center"
                >
                  <nuxt-img class="w-1/2" src="/icon.png" />
                </NuxtLink>
              </div>
              <div>
                <button
                  aria-label="Close Menu"
                  title="Close Menu"
                  class="p-2 -mt-2 -mr-2 transition duration-200 rounded hover:bg-gray-200 focus:bg-gray-200 focus:outline-none focus:shadow-outline"
                  @click="isMenuOpen = false"
                >
                  <svg class="w-5 text-gray-600" viewBox="0 0 24 24">
                    <path
                      fill="currentColor"
                      d="M19.7,4.3c-0.4-0.4-1-0.4-1.4,0L12,10.6L5.7,4.3c-0.4-0.4-1-0.4-1.4,0s-0.4,1,0,1.4l6.3,6.3l-6.3,6.3 c-0.4,0.4-0.4,1,0,1.4C4.5,19.9,4.7,20,5,20s0.5-0.1,0.7-0.3l6.3-6.3l6.3,6.3c0.2,0.2,0.5,0.3,0.7,0.3s0.5-0.1,0.7-0.3 c0.4-0.4,0.4-1,0-1.4L13.4,12l6.3-6.3C20.1,5.3,20.1,4.7,19.7,4.3z"
                    ></path>
                  </svg>
                </button>
              </div>
            </div>
            <nav>
              <ul class="space-y-4">
                <li>
                  <NuxtLink
                    to="/blog"
                    aria-label="Blog"
                    title="Blog"
                    class="font-medium tracking-wide text-gray-700 transition-colors duration-200"
                    >Blog</NuxtLink
                  >
                </li>
                <li>
                  <NuxtLink
                    to="/servicios"
                    aria-label="Servicios"
                    title="Servicios"
                    class="font-medium tracking-wide text-gray-700 transition-colors duration-200"
                    >Servicios</NuxtLink
                  >
                </li>
                <li>
                  <NuxtLink
                    to="/paquetes"
                    aria-label="Paquetes"
                    title="Paquetes"
                    class="font-medium tracking-wide text-gray-700 transition-colors duration-200"
                    >Paquetes</NuxtLink
                  >
                </li>
              </ul>
              <span class="flex mt-5 justify-center">
                <a v-if="ios" href="fb://profile/106070931823082">
                  <nuxt-img
                    class="mx-5 text-3xl w-8"
                    src="/icons/facebook-brands.svg"
                  />
                </a>

                <a v-else-if="android" href="fb://page/106070931823082">
                  <nuxt-img
                    class="mx-5 text-3xl w-8"
                    src="/icons/facebook-brands.svg"
                  />
                </a>

                <a v-else href="https://facebook.com/cintaticmx">
                  <nuxt-img
                    class="mx-5 text-3xl w-8"
                    src="/icons/facebook-brands.svg"
                  />
                </a>
                <a href="https://instagram.com/cintaticmx">
                  <nuxt-img
                    class="mx-5 text-3xl w-8"
                    src="/icons/instagram-brands.svg"
                  />
                </a>
                <a href="https://instagram.com/cintaticmx">
                  <nuxt-img
                    class="mx-5 text-3xl w-8"
                    src="/icons/whatsapp-brands.svg"
                  />
                </a>
                <a href="tel:5628348062">
                  <nuxt-img
                    class="mx-5 text-3xl w-8"
                    src="/icons/facebook-brands.svg"
                  />
                </a>
              </span>
            </nav>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
      ios: null,
      android: null,
    };
  },
  watch: {
    $route() {
      this.isMenuOpen = false;
    },
  },
  mounted() {
    if (navigator.userAgent.toLowerCase().includes("iphone")) this.ios = true;
    if (navigator.userAgent.toLowerCase().includes("android"))
      this.android = true;
  },
};
</script>
