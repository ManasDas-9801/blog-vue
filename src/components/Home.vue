<template>
    <div>
         <h1>Users Details</h1>
        <table border="2px">
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Email</th>
          </tr>
          <tr v-for="user in users" :key="user.id">
                  <td>{{user.id}}</td>
                  <td>{{user.name}}</td>
                  <td>{{user.email}}</td>
          </tr>
        </table>
    </div>
</template>

<script>
export default {
  name: 'Home',
  props:{
        data:String
      },
      data()
      {
        return{
          users:[
            {id:1,name:'peter',email:'peter@gmail.com'},
            {id:2,name:'akon',email:'akon@gmail.com'},
            {id:3,name:'dkon',email:'dkon@gmail.com'},
            {id:4,name:'bkon',email:'bkon@gmail.com'},
          ]
        }
      }
 
};
</script>
