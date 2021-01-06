<template>
  <main>
    <about />
    <skills />
    <experiences />
    <blogs />
  </main>
</template>

<template>
  <button @click="show = !show">
    Toggle
  </button>
  <transition name="fade">
    <p v-if="show">hello</p>
  </transition>
</template>

<script>
import About from '@/pages/about'
import Experiences from '@/pages/experiences'
import Skills from '@/pages/skills'
import Blogs from '@/pages/blogs'

export default {
  components: {
    About,
    Experiences,
    Skills,
    Blogs
  }
}
</script>

<script>const Demo = {
  data() {
    return {
      show: true
    }
  }
}

Vue.createApp(Demo).mount('#demo')</script>

<style>
main {
  margin-top: 1%;
}

body {
  margin: 30px;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s ease;
}

.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>
