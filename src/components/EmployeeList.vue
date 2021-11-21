<template>
   <div>
        <h2>This is Employee List </h2>
          <table border="2px">
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Email</th>
          </tr>
          <tr v-for="user in users" :key="user.id">
                  <td>{{user.id}}</td>
                  <td>{{user.e_firstname}}</td>
                  <td>{{user.e_lastname}}</td>
                  <td>{{user.e_email}}</td>
          </tr>
        </table>
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
         return {users:undefined} 
    },
    mounted(){
          Vue.axios.get('http://127.0.0.1:8000/api/check').then((res)=>{
              this.users = res.data.data;
               console.log(res.data.data)
          });
    }
}
</script>