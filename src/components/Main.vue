<template>
    <main class="bg-main d-flex align-items-center">
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
  }

</style>
