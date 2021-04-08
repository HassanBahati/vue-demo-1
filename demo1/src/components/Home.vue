<template>
    <div>
        <!-- <h1> Welcome to home Component </h1> -->
        <Header/>
        <BodyComponent/>
    </div>
</template>

<script>
import Header from './Header.vue'
import BodyComponent from './BodyComponent.vue'
    export default{
        name:'Home',
        components: {
            Header,
            BodyComponent
        }
    }
</script>

<style scoped>

</style>
