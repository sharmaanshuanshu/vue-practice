<template>
<h1>{{ msg }}</h1>
<h2>{{msg2}}</h2>
<h1 v-on:mousemove="getConsole()">{{name}}</h1>
<h1>{{getLastName()}}</h1>
<h1>{{email}}</h1>
<h1>{{ph}}</h1>
<!-- <h3>{{ getSum(10,10) }}</h3> -->
<button v-on:click="getAddress('Button 1')">Click</button>
<button v-on:dblclick="getAddress('Button double click')">Click Me</button>
<h1>Count {{ count }}</h1>
<button v-on:click="incrementCount()">Increment</button>
<button v-on:click="decrementCount()">Decrement</button><br /><br />

<!-- two way binding -->
<!-- Get Input tag value -->
<!-- v-on = @ -->
<input type="number" @:change="countValue" value="0" v-model="count" />

<!-- Get CheckBox with the help of v-model-->

<h1>Course</h1>
<label for="js">JavaScript</label>
<input type="checkbox" value="javaScript" id="js" v-model="technology" /><br />

<label for="react">React</label>
<input type="checkbox" value="react" id="react" v-model="technology" /><br />

<label for="next">Next Js</label>
<input type="checkbox" value="next" id="next" v-model="technology" />

<!-- Get Radio Button Value with the help of v-model  -->
<h1>Prifle</h1>
<label for="student">Student</label>
<input type="radio" value="student" id="student" v-model="who" name="who" />

<label for="developer">Developer</label>
<input type="radio" value="developer" id="developer" v-model="who" name="who" />

<h4>Technology: {{technology}}</h4>
<h4>I am a: {{who}}</h4>

<!--If Else-->

<h1 v-if="show">If Condition</h1>
<h1 v-else>Else Condition</h1>

<button v-on:click="show = !show">{{this.show == true ? 'Else' : 'If'}}</button>

<ul>
    <li v-for="item in username" :key="item">
        {{ item }}
    </li>
</ul>

<br />
<br />
<br />

<ul>
    <li v-for="item in userdata" :key="item.id">
        {{ item.id }}
        {{ item.name }}
        {{ item.Profile }}

    </li>
</ul>
<DerivedComponent name="Ankush Sharma" :userdetail="userdata" :getSum="getSum"></DerivedComponent>
</template>

<script>
import DerivedComponent from './DerivedComponent.vue';
export default {
    name: 'HomePage',
    components: {
        DerivedComponent
    },
    props: {
        msg: String,
        msg2: String
    },
    data() {
        return {
            name: 'Ankush',
            getLastName: function () {  
                return 'Sharma'
            },
            email: 'ak123@gmail.com',
            ph: '**********',
            count: 0,
            technology: [],
            who: null,
            show: false,
            username: ['Parminder', 'Chandra', 'Ankush', 'Jaskaran'],
            userdata: [{
                id: 1,
                name: 'Parminder',
                Profile: 'FrontEnd developer'
            }, {
                id: 2,
                name: 'Chandra',
                Profile: 'Designer'
            }, {
                id: 3,
                name: 'Jaskaran',
                Profile: 'BackEnd developer'
            }, {
                id: 4,
                name: 'Ankush',
                Profile: 'FrontEnd developer'
            }, ]
        }
    },
    methods: {
        getSum(a, b) {
            console.log('getSum...........')
            var sum = a + b;
            return sum;
        },
        getAddress(data) {
            console.log(data);
        },
        getConsole() {
            console.log('Mouse Move.............');
        },
        incrementCount() {
            this.count = this.count + 1;
        },
        decrementCount() {

            this.count = this.count - 1;
            if (this.count < 0) {
                this.count = 0;
            }
        },
        countValue(event) {
            console.log(event.target.value)
            if (this.count < 0) {
                this.count = 0;
            }
        }
    }
}
</script>

<style scoped>
/*scoped property bind our property with particular component*/
h1 {
    color: orange;
}
</style>
