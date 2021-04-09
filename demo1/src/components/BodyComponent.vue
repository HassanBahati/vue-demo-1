<template>
  <div class="container">
    <div class="row" style="text-align:left">
      <div class="col-4">
        <h3>Student Registration Form</h3>
        <hr />
        <h5>{{studentName}}</h5>
        <div class="input-group mb-3">
          <div class="input-group mb-3">
            <input
              type="text"
              class="form-control"
              placeholder="Student's username"
              aria-label="Student's username"
              aria-describedby="basic-addon2"
              v-model="studentName"
            />
            <div class="input-group-append">
              <button class="btn btn-primary" type="button">Register</button>
            </div>
          </div>
        </div>
      </div>
      <div class="col-8">
        <h3>Student Registration List</h3>
        <ol class="list-group list-group-numbered">
          <!-- v-bind can be represented with full colon  ---interpolating with 2 braces to avoid hard coding info  -->
          <li class="list-group-item" v-for="student in students" :key='student'>{{student}}</li>
        </ol>
      </div>
    </div>
  </div>
  <!-- research about slots in vue js
  v-modal --2 way data binding --eg used on input fields to dynamically makely changes  -->
</template>


<script>
export default {
  name: "BodyComponent",
  data() {
    return {
      students:[],
      studentName: ''
    };
  },
  methods: {},
  components: {},
};
</script>



<style scoped>
</style>