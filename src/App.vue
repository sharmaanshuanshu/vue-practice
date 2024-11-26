<template>
<!-- <HelloWorld msg="Welcome to Your Vue.js App" />
<HomePage msg2="Welcome to Vue Tutorial" />

<ul>
    <li v-for="item in userDetail" :key="item.firstName">
        <UserPage :data="item" :nameFuncation="getAddress"></UserPage>
    </li>
</ul> -->
<!-- <HtmlBinding></HtmlBinding>
<ClassBinding></ClassBinding> -->
<h1>App Vue</h1>
<!-- <ChildComponent></ChildComponent> -->
<ParentComponent></ParentComponent>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

// import ChildComponent from './components/ChildComponent.vue';

// import ClassBinding from './components/ClassBinding.vue';
// import HelloWorld from './components/HelloWorld.vue'
// import HomePage from './components/HomePage.vue'
// import HtmlBinding from './components/HtmlBinding.vue';
// import UserPage from './components/UserPage.vue';

export default {
    name: 'App',
    components: {
        // HelloWorld,
        // HomePage,
        // UserPage,
        // HtmlBinding,
        // ClassBinding
        // ChildComponent
        ParentComponent
        
    },
    data() {
        return {
            userDetail: [{
                    firstName: 'Suresh',
                    lastName: 'Sharma'
                },
                {
                    firstName: 'Naresh',
                    lastName: 'Sharma'
                }, {
                    firstName: 'Ankush',
                    lastName: 'Sharma'
                }
            ]
        }
    },
    methods: {
        getAddress: function (name) {
            alert(name);
        }
    }
}
</script>
