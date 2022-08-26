<template>
  <DefaultLayout>
    <section class="slider py-5">
      <ul class="flex justify-center gap-4 mb-2.5">
        <li class="rounded-full cursor-pointer px-5 py-1.5 text-white" v-on:click="tab = 0" v-bind:class="{'bg-white text-black': tab === 0}">Okul Alışverişi</li>
        <li class="rounded-full cursor-pointer px-5 py-1.5 text-white" v-on:click="tab = 1" v-bind:class="{'bg-white text-black': tab === 1}">Sana Özel</li>
        <li class="rounded-full cursor-pointer px-5 py-1.5 text-white" v-on:click="tab = 2" v-bind:class="{'bg-white text-black': tab === 2}">Bugüne Özel</li>
        <li class="rounded-full cursor-pointer px-5 py-1.5 text-white" v-on:click="tab = 3" v-bind:class="{'bg-white text-black': tab === 3}">Kampanyalar</li>
        <li class="rounded-full cursor-pointer px-5 py-1.5 text-white" v-on:click="tab = 4" v-bind:class="{'bg-white text-black': tab === 4}">Kaçırılmayacak Fırsatlar</li>
        <li class="rounded-full cursor-pointer px-5 py-1.5 text-white" v-on:click="tab = 5" v-bind:class="{'bg-white text-black': tab === 5}">Ayrıcalıklar</li>
      </ul>
      <div class="slider-container container">
        <div class="slider-items h-full bg-white rounded-lg p-1 cursor-default" v-bind:class="{'block': tab === 0, 'hidden': tab !== 0}">
          <div class="flex items-center h-full">
            <div class="lg:w-5/12 xl:w-[34.853333%] h-full px-12 py-16 mt-2">
              <h3 class="text-2xl mb-2">Çocuklar için maske, sağlık ve</h3>
              <h3 class="text-3xl font-semibold leading-tight mb-8">hijyen ürünlerinde özel fırsatlar</h3>
              <router-link to="/" class="bg-violet-700 rounded-full py-3 px-4 text-white">Acele et kaçırma</router-link>
            </div>
            <div class="lg:w-7/12 xl:w-[65.146667%] h-full bg-neutral-300 rounded-lg">
              <img src="../assets/img/banner/bannerImage2140_20220818115530.webp" class="w-full h-full rounded-lg" alt="">
            </div>
          </div>
        </div>
        <div class="slider-items h-full bg-white rounded-lg p-1 cursor-default" v-bind:class="{'block': tab === 1, 'hidden': tab !== 1}">
          <div class="flex items-center h-full">
            <div class="lg:w-5/12 xl:w-[34.853333%] h-full px-12 py-16 mt-2">
              <h3 class="text-2xl mb-2">1 - Çocuklar için maske, sağlık ve</h3>
              <h3 class="text-3xl font-semibold leading-tight mb-8">hijyen ürünlerinde özel fırsatlar</h3>
              <router-link to="/" class="bg-violet-700 rounded-full py-3 px-4 text-white">Acele et kaçırma</router-link>
            </div>
            <div class="lg:w-7/12 xl:w-[65.146667%] h-full bg-neutral-300 rounded-lg">
              <img src="../assets/img/banner/bannerImage2140_20220818115530.webp" class="w-full h-full rounded-lg" alt="">
            </div>
          </div>
        </div>
        <div class="slider-items h-full bg-white rounded-lg p-1 cursor-default" v-bind:class="{'block': tab === 2, 'hidden': tab !== 2}">
          <div class="flex items-center h-full">
            <div class="lg:w-5/12 xl:w-[34.853333%] h-full px-12 py-16 mt-2">
              <h3 class="text-2xl mb-2">2 - Çocuklar için maske, sağlık ve</h3>
              <h3 class="text-3xl font-semibold leading-tight mb-8">hijyen ürünlerinde özel fırsatlar</h3>
              <router-link to="/" class="bg-violet-700 rounded-full py-3 px-4 text-white">Acele et kaçırma</router-link>
            </div>
            <div class="lg:w-7/12 xl:w-[65.146667%] h-full bg-neutral-300 rounded-lg">
              <img src="../assets/img/banner/bannerImage2140_20220818115530.webp" class="w-full h-full rounded-lg" alt="">
            </div>
          </div>
        </div>
        <div class="slider-items h-full bg-white rounded-lg p-1 cursor-default" v-bind:class="{'block': tab === 3, 'hidden': tab !== 3}">
          <div class="flex items-center h-full">
            <div class="lg:w-5/12 xl:w-[34.853333%] h-full px-12 py-16 mt-2">
              <h3 class="text-2xl mb-2">3 - Çocuklar için maske, sağlık ve</h3>
              <h3 class="text-3xl font-semibold leading-tight mb-8">hijyen ürünlerinde özel fırsatlar</h3>
              <router-link to="/" class="bg-violet-700 rounded-full py-3 px-4 text-white">Acele et kaçırma</router-link>
            </div>
            <div class="lg:w-7/12 xl:w-[65.146667%] h-full bg-neutral-300 rounded-lg">
              <img src="../assets/img/banner/bannerImage2140_20220818115530.webp" class="w-full h-full rounded-lg" alt="">
            </div>
          </div>
        </div>
        <div class="slider-items h-full bg-white rounded-lg p-1 cursor-default" v-bind:class="{'block': tab === 4, 'hidden': tab !== 4}">
          <div class="flex items-center h-full">
            <div class="lg:w-5/12 xl:w-[34.853333%] h-full px-12 py-16 mt-2">
              <h3 class="text-2xl mb-2">4 - Çocuklar için maske, sağlık ve</h3>
              <h3 class="text-3xl font-semibold leading-tight mb-8">hijyen ürünlerinde özel fırsatlar</h3>
              <router-link to="/" class="bg-violet-700 rounded-full py-3 px-4 text-white">Acele et kaçırma</router-link>
            </div>
            <div class="lg:w-7/12 xl:w-[65.146667%] h-full bg-neutral-300 rounded-lg">
              <img src="../assets/img/banner/bannerImage2140_20220818115530.webp" class="w-full h-full rounded-lg" alt="">
            </div>
          </div>
        </div>
        <div class="slider-items h-full bg-white rounded-lg p-1 cursor-default" v-bind:class="{'block': tab === 5, 'hidden': tab !== 5}">
          <div class="flex items-center h-full">
            <div class="lg:w-5/12 xl:w-[34.853333%] h-full px-12 py-16 mt-2">
              <h3 class="text-2xl mb-2">5 - Çocuklar için maske, sağlık ve</h3>
              <h3 class="text-3xl font-semibold leading-tight mb-8">hijyen ürünlerinde özel fırsatlar</h3>
              <router-link to="/" class="bg-violet-700 rounded-full py-3 px-4 text-white">Acele et kaçırma</router-link>
            </div>
            <div class="lg:w-7/12 xl:w-[65.146667%] h-full bg-neutral-300 rounded-lg">
              <img src="../assets/img/banner/bannerImage2140_20220818115530.webp" class="w-full h-full rounded-lg" alt="">
            </div>
          </div>
        </div>
      </div>
      <div class="container text-center mt-6">
        <button class="py-1 px-4 border-2 rounded-full border-white text-white" v-on:click="tab > 0 ? tab -= 1 : tab = 0">←</button>
        <button class="py-1 px-4 border-2 rounded-full border-white text-white ml-4" v-on:click="tab < 5 ? tab += 1 : tab = 0">→</button>
      </div>
    </section>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </DefaultLayout>
</template>

<script>
// @ is an alias to /src
import DefaultLayout from '@/layouts/Default.vue'

export default {
  name: 'HomeView',
  components: {
    DefaultLayout
  },
  data () {
    return {
      tab: 0
    }
  }
}
</script>

<style lang="scss">
.slider {
  background-color: #aaaaaa;
  background-image: linear-gradient(180deg, #aaaaaa 0%, #cfcfcf 24%, #dddddd 100%);
  // height: 56.9vh;
  height: 540px;
  max-height: 540px;

  .slider-container {
    height: calc(540px - 9.75rem)!important;
  }
}
</style>
