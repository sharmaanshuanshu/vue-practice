<template>
<h2>Derived Component</h2>
<h2>{{ name }}</h2>
<ul>
    <li v-for="item in userdetail" :key="item.id">
        {{ item.name }} &nbsp;
        {{ item.Profile }}
    </li>
</ul>

<button v-on:click="getSum; show = true">Get Sum</button>

<h1 v-if="show">{{ getSum(15,15) }}</h1>
<h1 v-else>Error</h1>
</template>

<script>
export default {
    name: 'DerivedComponent',
    props: {
        name: String,
        userdetail: Object,
        getSum: Function,
    },

    data() {
        return{
            show: false
        }
    }
}
</script>
