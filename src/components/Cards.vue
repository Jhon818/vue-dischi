<template>
<section class="container">
   
<ul class="row">
      <li class="col-xl-2 col-lg-2 col-sm-5 text-center m-3 p-2" v-for="(card,index) in cardsList" :key="index">
<img class="w-100" :src="card.poster" alt="">

<div class="d-flex flex-column">
         <span class="text-light">{{card.title}}</span>
         <span>{{card.author}}</span>
         <span>{{card.year}}</span>
</div>
       
      </li>
  </ul>

</section>
</template>

<script>
// import Search from '@/components/Search.vue';
import axios from 'axios';
export default {
  name: 'Cards',
//   components : {
//       Search,
//   },
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
        },
    }
}
</script>

<style lang="scss">



li {
    background: rgb(13, 12, 36);
    list-style: none;
}

span {
    color: grey;
}
</style>