<template>
  <div class="index-page bg-grey-2 window-height window-width column items-center no-wrap">
    <div class="banner bg-primary flex flex-center">
      Vue Cesium Demo
    </div>
    <div class="text-center">
      <div class="card bg-white shadow-4 column no-wrap flex-center group q-gutter-sm">
        <img src="https://zouyaoji.top/vue-cesium/favicon.png" class="responsive">
        <q-btn
          color="primary"
          push
          @click="$router.push('/showcase')"
          class="full-width"
          icon="layers"
        >
          {{ $t('index.showcase') }}
        </q-btn>

        <q-btn
          color="secondary"
          push
          class="full-width"
          @click="launch('https://zouyaoji.top/vue-cesium')"
          icon="launch"
        >
          {{ $t('index.docs') }}
        </q-btn>
      </div>
    </div>
    <a class="ribbon cursor-pointer" @click="launch('https://github.com/zouyaoji/vue-cesium-demo')" :title="`Fork me on github`"></a>
  </div>
</template>

<script>
import { openURL } from 'quasar'
export default {
  components: {
  },
  methods: {
    launch (url) {
      openURL(url)
    }
  }
}
</script>

<style>
.index-page .banner {
  height: 50vh;
  width: 100%;
  font-size: 12vmax;
  color: rgba(255,255,255,0.2);
  overflow: hidden;
}
.index-page .card {
  width: 80vw;
  max-width: 500px;
  padding: 10px 25px;
  margin-top: -90px;
  border-radius: 2px;
}
.index-page .card img {
  height: 128px;
  width: 128px;
}
.ribbon {
  width: 12.1em;
  height: 12.1em;
  position: absolute;
  overflow: hidden;
  top: 0;
  right: 0;
  z-index: 39;
  pointer-events: none;
  font-size: 15px;
  text-decoration: none;
  text-indent: -999999px;
  opacity: 0.7;
}
.ribbon.fixed {
  position: fixed;
}
.ribbon:before {
  content: '';
  padding: 0.38em 0;
  background-color: #fff;
  background-image: linear-gradient(to bottom, rgba(0,0,0,0), rgba(0,0,0,0.15));
  box-shadow: 0 0.15em 0.23em 0 rgba(0,0,0,0.5);
  pointer-events: auto;
}
.ribbon:after {
  content: attr(title);
  color: #027be3;
  line-height: 1.54em;
  text-decoration: none;
  text-align: center;
  text-indent: 0;
  padding: 0.15em 0;
  margin: 0.15em 0;
}
.ribbon:before,
.ribbon:after {
  position: absolute;
  display: block;
  width: 15.38em;
  height: 1.74em;
  top: 3.23em;
  right: -3.23em;
  transform: rotate(45deg);
}

</style>
