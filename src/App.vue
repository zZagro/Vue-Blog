<template>
  <Sidebar/>
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
:root {
  --clr-indigo950: #1e1b4b;
  --clr-indigo800: #3730a3;
  --clr-indigo700: #4338ca;
  --clr-indigo600: #4f46e5;
  --clr-indigo500: #6366f1;
  --clr-indigo300: #a5b4fc;
}

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