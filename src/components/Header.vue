<template>
  
    <header class="bg-header">
      <img class="width-logo" alt="spotify" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/768px-Spotify_logo_without_text.svg.png">
      <Search  @search='getCards'/>
    </header>
 
</template>

<script>
import Search from '@/components/Search.vue';

export default {
  name: 'Header',
  components: {
      Search,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/general.scss";

  .bg-header {
    padding: 6px;
    background:rgb(8, 8, 66);
  }

</style>
