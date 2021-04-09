<template>
  <div class="container">
    <div class="row" style="text-align: left">
      <div class="col-4">
        <h3>Student Registration Form</h3>
        <hr />
        <h5>{{ studentName }}</h5>
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
              <button class="btn btn-primary" type="button" v-on:click='registerStudent'>Register</button>
            </div>
          </div>
        </div>
      </div>
      <!-- no colon before the unique key because we dont intend to bind it any attribute   -->
      <div class="col-8">
        <StudentList :students='students' uniqueKey="1" optionalProperty="Specified" /> 
        <StudentList :students='students' uniqueKey="2"/> 
      </div>
    </div>
  </div>
  <!-- research about slots in vue js
  v-modal --2 way data binding --eg used on input fields to dynamically makely changes  -->
</template>


<script>
import StudentList from './studentList.vue'
export default {
  name: "BodyComponent",
  data() {
    return {
      students: [],
      studentName: "",
    };
  },
  methods: {
    validateForm: function(){
      //this.studentName- then you pass in your vaidaltions 
    },
    //function to add a name to the list of students 
    registerStudent: function(){
      this.students.push(this.studentName)
    }
  },
  components: {StudentList},
  
};
</script>



<style scoped>
</style>