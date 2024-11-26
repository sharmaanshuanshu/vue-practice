<template>
<div class="user">
    <h3>{{ data.firstName }}</h3>
    <h3>{{ data.lastName }}</h3>
    <button v-on:click="nameFuncation(data.firstName)">Alert Name</button>
</div>
</template>

<script>
export default {
    name: 'UserPage',
    props: {
        data: Object,
        nameFuncation: Function
    },
    data() {

    },
    methods: {
        render: function () {
            console.log('render...........');
        },
        // getAddress: function(){

        // }
    }
}
</script>

<style>
.user {
    background-color: aquamarine;
}
</style>
