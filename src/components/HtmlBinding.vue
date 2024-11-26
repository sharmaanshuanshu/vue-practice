<template>
    <h1>{{ text }}</h1>
    <div v-html="tag"></div>
    <div v-html="tag2"></div>
</template>

<script>

    export default{
        name: 'HtmlBinding',
        data(){
            return{
                text: 'Html Binding',
                tag: '<h3>Welcome to code step by step</h3>',
                tag2: '<h3>This is vue js tutorial</h3>'
            }
        }
    }
</script>