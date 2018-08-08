<template>
  <section>
    <model-gltf
      :backgroundAlpha="0"
      src="static/models/gltf/samplerhorn.gltf"
      @on-load="onLoad"
      :lights="lights"
      backgroundColor="#000"></model-gltf>
    <div class="example-loading" v-show="loading"></div>
  </section>
</template>

<script>
    import { ModelGltf } from 'vue-3d-model'

    export default {
      data() {
        return {
          loading: true,
          // lights: [255,255,255]
        }
      },
      methods: {
        onLoad() {
          this.loading = false;
        }
      },
      components: {
          ModelGltf
      }
    }
</script>
