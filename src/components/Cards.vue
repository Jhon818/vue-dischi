<template>
<section class="container">
 <ul class="row">
      <li class="col-3" v-for="(card,index) in cardsList" :key="index">
<div>{{card.poster}}</div>
        <p>{{card.title}}</p>
        <p>{{card.year}}</p>
      </li>
  </ul>
</section>
</template>

<script>

import axios from 'axios';
export default {
  name: 'Cards',
    data() {
        return {  APIurl: "https://flynn.boolean.careers/exercises/api/array/music",
         cardsList: []
         }
    },
    created() {
        this.getCards()
    },
    methods: {
        getCards() {
            axios
                .get(this.APIurl)
                    .then( res => {
                        this.cardsList = res.data.response;
                    })
        }
    }
}
</script>

<style>

</style>