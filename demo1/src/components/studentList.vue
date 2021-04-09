<template>
    <div>
        <h3>Student Registration List {{uniqueKey }} {{optionalProperty}}</h3>
        <ol class="list-group list-group-numbered">
          <!-- v-bind can be represented with full colon  ---interpolating with 2 braces to avoid hard coding info  -->
          
          <!-- onSubit 
          onClick

           -->
          <li
            class="list-group-item"
            v-for="student in students"
            :key="student"
          >
            {{ student }}
          </li>
        </ol>
    </div>
</template>

<script>


export default{
    name:'StudentList',
    props:{
    students: {type:Array},
    uniqueKey: {type: Number},
    optionalProperty: {type:String, default:'Default'}
  }
};
</script>
