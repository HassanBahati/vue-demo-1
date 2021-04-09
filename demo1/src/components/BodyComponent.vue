<template>
  <div>
    <h3 v-if="state">Bulb ON</h3>
    <h3 v-else>Bulb OFF</h3>

    <button type="button" class="btn btn-secondary" v-on:click="changeState">
      <span v-if="state">Turn Off</span>
      <span v-else>Turn On</span>
    </button>
  </div>
</template>


<script>
export default {
  name: "BodyComponent",
  data: function () {
    return {
      state: false,
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