<template>
  <div class="body">
    <meu-menu :rotas="routes" />
    <transition name="pagina">
    <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import { routes } from './routes'
import Menu from './components/shared/menu/Menu.vue'
export default {
  data() {
    return {
      routes,
    }
  },

  components: {
    'meu-menu': Menu,
  }
}
</script>

<style>
.body {
  font-family: Helvetica, sans-serif;
  margin: 0 auto;
  width: 96%;
}

.pagina-enter, .pagina-leave-active {
  opacity: 0;
}

.pagina-enter-active, .pagina-leave-active {
  transition: opacity 0.3s;
}
</style>