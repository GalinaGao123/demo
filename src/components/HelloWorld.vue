<template>
  <div class="hello">
    <icon type="waiting" />
    <div class="breathe"></div>
  </div>
</template>

<script>
import { Icon } from 'vux'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    Icon
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@keyframes breathe {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
    transform: scale3d(1.3, 1.3, 1.3);
  }
}
.hello {
  background-color: #0fdcff;
  width: 80px;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ffffff;
  margin: 0 auto;
  position: relative;
}

.breathe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(15, 220, 255, 0.4);
  animation: breathe 2s ease-in-out infinite;
}
</style>
