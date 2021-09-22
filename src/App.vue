<template>
  <div id="app">
    <Header />
    <Main />
    <Cards />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from '@/components/Main.vue'
import Cards from '@/components/Cards.vue'
export default {
  name: 'App',
  components: {
    Header,
    Main,
    Cards
  }
}
</script>

<style lang="scss">
@import "/style/general.scss";

  #app {
    width: 100vw;
    height: 100vh;

    img.width-logo {
      width: 2rem;
    }
  }
</style>
