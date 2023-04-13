<template>
  <Sidebar />
  <div class="router" :style="{ 'margin-left': sidebarWidth }">
    <router-view/>
  </div>
</template>

<script>
import Sidebar from './components/nav/Sidebar'
import { sidebarWidth } from './components/nav/state'

export default {
  components: {
    Sidebar,
  },
  setup() {
    return {
      sidebarWidth
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.router {
  transition: all 0.3s ease;
}
</style>