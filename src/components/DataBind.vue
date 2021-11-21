<template>
    <div>
        <h1>{{name}}</h1>
        <input type="text" v-model="name" />
    </div>
</template>

<script>
export default {
     name:"HomeBind",
    data(){
        return {
            name:'This is message',
           
        }
    }
}
</script>