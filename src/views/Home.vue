<template>
  <div class="home">
    <img v-x:click="woshini" alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
    directives:{
    'x':{
      inserted:function(el,info){
        console.log(info)
        el.addEventListener(info.arg,info.value)
      }
    }
  },
  components: {
    HelloWorld
  },
  methods:{
    woshini(){console.log('hi')}
  }
}
</script>
