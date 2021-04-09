<template>
  <div>
    <!-- <h1 v-if="mark>49">Passed</h1>
    <h1 v-else-if="mark<50">Failed</h1>
    <h1 v-else>Ungraded</h1> -->
    <!-- v-if used when want to add conditional 
    similar to 
    checkout v-if-(visibility-none/block)
     versus
      v-show -(display-visible/hidden)-->
  <ul>
    <li v-for="fruit in fruits" v-bind:key="fruit">{{fruit}}</li>
    <!-- <li>oranges</li>
    <li>mangoes</li>
    <li>pineapples</li>
    <li>grapes</li>
    <li>jackfruits</li>
    <li>guavas</li>
    <li>strawberries</li>
    <li>blackberries</li>
    <li>olives</li>
    <li>cashewnuts</li> -->
  </ul>



  </div>
</template>

<script>
export default {
  name: "Body",
  data: function(){
      return{
          mark: 60,
          fruits: ['apples','oranges', 'mangoes', 'pineapples', 'grapes','jackfruits', 'guavas', 'strawberries', 'blackberries', 'olives', 'cashewnuts', 50]
      }
  }
};
</script>

<style scoped>
</style>