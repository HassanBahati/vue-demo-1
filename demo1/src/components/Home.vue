<template>
    <div>
        <!-- <h1> Welcome to home Component </h1> -->
        <Header/>
        <BodyComponent/>
        <FooterComponent/>
    </div>
</template>

<script>
import Header from './Header.vue'
import BodyComponent from './BodyComponent.vue'
import FooterComponent from './FooterComponent.vue'
    export default{
        name:'Home',
        components: {
            Header,
            BodyComponent,
            FooterComponent
        }
    }
</script>

<style scoped>

</style>
