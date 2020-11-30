<template>
  <div class="home">
    <div class=image-box>
      <img alt="Vue logo" src="../assets/logo.png">
    </div>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss">
.image-box{
  background: lightblue;
  height: 8em;
  margin-bottom: 5em;

    img{
      transform: scaleY(1);
      animation: imgExpand 1s;
    }

    @keyframes imgExpand {
      from{transform:scaleY(0)}
    }
}
</style>