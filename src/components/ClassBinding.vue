<template>
<h1 :class="{ green: colorfull}">ClassBinding</h1>
<h3 :class="applyStyle">Dynamic Classes</h3>
<button v-on:click="colorfull = !colorfull">{{!colorfull ? 'ApplyCls' : 'RemoveCls' }}</button>
</template>

<script>
export default {
    name: 'ClassBinding',
    data() {
        return {
            colorfull: true
        }
    },
    computed: {
        applyStyle() {
            return {
                green: this.colorfull,
                err: true,
                textSize: true
            }
        }
    }
}
</script>

<style>
.green {
    background-color: green;
    width: 200px;
}

.err {
    color: red;
}

.textSize {
    font-size: 400px;
}
</style>
