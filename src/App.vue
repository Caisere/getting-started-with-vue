<template>
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <UserAvatar/>
    <HelloWorld msg="Welcome to Your Vue.js App" name="Omoshola"/>
    <VueDirectives/> -->
    <FormComponent/>
    <!-- <div class="footer">
        <FooterComponent/>
    </div> -->
</template>

<script>
// import FooterComponent from './components/Footer.vue';
// import HelloWorld from './components/HelloWorld.vue'
// import UserAvatar from './components/Avatar.vue';
// import VueDirectives from './components/Directives.vue';
import FormComponent from './components/FormComponent.vue';

export default {
    name: 'App',
    components: {
        // HelloWorld,
        // UserAvatar,
        // VueDirectives,
        // FooterComponent,
        FormComponent
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

template {
    display: flex;
    flex-direction: column;
    align-items: center;
}

</style>
