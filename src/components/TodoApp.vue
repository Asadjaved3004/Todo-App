<template>
 <div class="container">
  <h1 class="text-center mt-5">My Vue Todo-App</h1>
  <!-------------Input-------->
  <div class="d-flex">
<input  v-model="task" type="text" placeholder="Enter task" class="form-control">
<button  @Click="submitTask" class="btn btn-warning rounded-0">Submit</button>
  </div>

  <!------------------Task Table------->

  <table class="table table-bordered mt-5">
  <thead>
    <tr>
      <th scope="col">Task</th>
      <th scope="col">Status</th>
      <th scope="col" class="text-center">#</th>
      <th scope="col" class="text-center">#</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(task,index) in tasks" :key="index">
      <td>{{ task.name }}</td>
      <td> {{ task.status }}</td>
      <td>
    <div class="text-center">
    <span class="fa fa-pen"></span>
    </div>
      </td>
      <td>
        <div class="text-center">
    <span class="fa fa-trash"></span>
    </div>
      </td>
    </tr>
  </tbody>
</table>

 </div>
</template>

<script>
export default {
  name: 'TodoApp',
  data(){
    return {
      task:'',
      tasks:[
        {
          name:'Steal Fruits from Store',
          status:'To-do'
        },
        {
          name:'Eat 1kg chocolate in 1 hour',
          status:'in-progress'
        }
      ]
    }
  },
  methods:{
    submitTask(){
      console.warn("Hello from submit Task");
    }
  }

}
</script>


