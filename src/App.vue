<template>
  <sample></sample>
</template>

<script>
import Sample from "./Sample.vue";

export default {
  name: 'app',
  components: { Sample },
}
</script>

<style>
body{
  background-color: #000;
}
.example-loading {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    text-align: center;
}
.example-loading::before {
    content: '';
    border-radius: 100%;
    margin: 2px;
    border: 3px solid #20a0ff;
    border-bottom-color: transparent;
    height: 36px;
    width: 36px;
    display: inline-block;
    animation: loading-rotate .75s 0s linear infinite;
    vertical-align: middle;
}
.example-loading::after {
    content: '';
    display: inline-block;
    height: 100%;
    width: 0;
    vertical-align: middle;
}
@keyframes loading-rotate{
    0% {
        transform: rotate(0) scale(1);
    }
    /* 50% {
        transform: rotate(180deg) scale(.6);
    } */
    100% {
        transform: rotate(360deg) scale(1);
    }
}
</style>
