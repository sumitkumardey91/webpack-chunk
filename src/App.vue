<template>
  <div id="app">
    <component :is="msg" />
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: ''
    }
  },
  mounted () {
    setTimeout(() => {
      this.msg = () => import(/* webpackChunkName: 'welcomeHere' */  './components/HelloWorld.vue')
    }, 2000)
  }
}
</script>


