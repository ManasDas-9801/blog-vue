<template>
   <div>
        <h2>This is Employee List </h2>
         <input type="text" v-model="name">
          <table border="2px">
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>User Possibility</th>
          </tr>
          <tr v-for="user in users" :key="user.id">
                  <td>{{user.country_id}}</td>
                  <td class="text-danger">{{name}}</td>
                  <td>{{user.probability}}</td>
                  <td>{{user.e_email}}</td>
          </tr>

        </table>

        <button v-on:click="get()">GEt</button>
   </div>
    
</template>

<script>
import Vue from 'vue';
import axios from 'axios';
import VueAxios from 'vue-axios';
Vue.use(VueAxios,axios);
export default {
    name:"EmployeeList",
    data(){
         return {users:undefined,name:''} 
    },
    methods:{
         get()
         {
               Vue.axios.get('https://api.nationalize.io/?name=' + this.name).then((res)=>{
              this.users = res.data.country;
              
               console.log(res);
          });
         }
    }
}
</script>