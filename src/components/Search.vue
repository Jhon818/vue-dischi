<template>
<div>
    <select class="form-select col-2 mb-3" aria-label=".form-select-lg example">
        <input type="text" class="" v-model="inputText">
        <option @click.prevent="$emit('search' , 'inputText')"></option>
    </select>

    <select class="form-select form-select-sm" aria-label=".form-select-sm example">
        <option selected>Open this select menu</option>
    </select>
</div>
</template>

<script>

export default {
    name: 'Search',
    data() {
        return {
            inputText: ""
        }
    },
    methods: {

    }
}
</script>

<style>

</style>