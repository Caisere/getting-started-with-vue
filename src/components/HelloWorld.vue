<template>
    <div class="hello">
        <div class="header">
            <Avatar />
            <h1>{{ name }}</h1>
        </div>
        <h3>{{isStudent ? 'A student of VueJs' : 'No, not a student of VueJs' }}</h3>
        <h1 v-show='isStudent'>{{ msg }}</h1>
        <p>{{ count }}</p>
        <!-- v-on:click (directive) = @click -->
        <button @click="increment">Increment</button>
    </div>
</template>

<script>
import Avatar from './Avatar.vue'
export default {
    name: 'HelloWorld',
    components: {
        Avatar
    },
    props: {
        msg: String,
        // Add any additional props you need here
        name: String
    },
    data() {
        return {
            count: 0,
            isStudent: true,
        }
    },
    methods: {
        increment(){
            this.count++
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }
    button {
        background-color: #42b983;
        color: white;
        border: none;
        padding: 10px 20px;
        cursor: pointer;
        border-radius: 4px;
    }
    .header {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 2rem
    }
</style>
