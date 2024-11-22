<template>
<HelloWorld msg="Welcome to Your Vue.js App" />
<HomePage msg2="Welcome to Vue Tutorial" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HomePage from './components/HomePage.vue'

export default {
    name: 'App',
    components: {
        HelloWorld,
        HomePage
    }
}
</script>
