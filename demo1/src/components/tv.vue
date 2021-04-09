<template>
  <div>
    <h3 v-if="state">Tv ON</h3>
    <h3 v-else>Tv OFF</h3>
<!-- v-on -- to set event handler  -->
    <button type="button" class="btn btn-secondary" v-on:click="changeState">
      <span v-if="state">Turn Off</span>
      <span v-else>Turn On</span>
    </button>
    &nbsp;
    <a v-bind:href='facebookLink'>Facebook</a> &nbsp;
    <!-- v-bind helps to bind variables to hmtl attributes so that they are not hard coded -->
    <a v-bind:href='googleLink'>Google</a>

    <img v-bind:src="television.source" v-bind:alt="television.alt">
  </div>
</template>


<script>
export default {
  name: "TvComponent",
  data: function () {
    return {
      state: false,
      //any variable name
      googleLink: 'https://www.google.com',
      facebookLink: 'https://www.facebook.com',
      television: {
        source: 'path',
       alt: 'Television'
      }
    };
  },
  methods: {
    //to change the state
    changeState: function () {
      //this to help us access what ever is in state
      // ! negation operator to turn state if its off or if state is off to turn it on
      this.state = !this.state;
    },
  },
};
</script>



<style scoped>
</style>