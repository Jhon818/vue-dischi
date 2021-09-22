<template>
    <main class="bg-main col-sm-6 col-lg-6 col-xl-12">
        <Cards />
    </main>
</template>

<script>
import Cards from '@/components/Cards.vue'

export default {
  name: 'Main',
  components: {
      Cards,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/general.scss";

  .bg-main {
    background: $bg-main-spotify;
    height: $h-100vh;
  }

</style>
