<template>
    <div>
        <h1>
            Template In Vue
        </h1>
        <h2>{{name}}</h2>
        <h2>{{age}}</h2>
        <button v-on:click="getAge()">Get age </button>
    </div>
</template>

<script>
export default {
    name:"Template",
    data(){
        return {
            name:'Manas',
            a:10,
            b:20,
            age:null
        }
    },
    methods:{
        getAge()
        {
            this.age=this.a+this.b;
        }
    }
}
</script>