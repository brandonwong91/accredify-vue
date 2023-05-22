<script>
import HomeView from '../views/HomeView.vue'
import NotFound from '../views/NotFound.vue'
import IconHome from './icons/IconHome.vue'
import IconNote from './icons/IconNote.vue'
import IconLightBulb from './icons/IconLightBulb.vue'
import IconShield from './icons/IconShield.vue'
import IconCog from './icons/IconCog.vue'

const routes = {
  '/': HomeView
}

export default {
  data() {
    return {
      currentPath: window.location.hash,
      activeClass: window.location.pathname === '/' ? 'bg-[#353D4E]' : '',
      navItemsClass: 'p-4 aspect-square hover:bg-[#353D4E] cursor-pointer'
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || NotFound
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
      this.currentPath = window.location.hash
    })
  },
  components: {
    IconHome,
    IconNote,
    IconLightBulb,
    IconShield,
    IconCog
  }
}
</script>

<template v-for:>
  <nav class="w- flex flex-col h-[100vh]">
    <div class="h-5 w-5 p-5 mx-[10px] my-4 rounded-full bg-white self-center" />
    <div class="grid place-content-center">
      <a href="/" :class="[navItemsClass, activeClass]">
        <IconHome />
      </a>
      <a href="/?user=1" :class="[navItemsClass]">
        <IconNote />
      </a>
      <a href="/?user=2" :class="[navItemsClass]">
        <IconLightBulb />
      </a>
      <div :class="[navItemsClass]">
        <IconShield />
      </div>
      <div :class="[navItemsClass]">
        <IconCog />
      </div>
    </div>
  </nav>
  <!-- <component :is="currentView" /> -->
</template>
