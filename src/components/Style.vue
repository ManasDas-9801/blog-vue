<template>
    <div>
        <h2 class="heading">
            This is class
        </h2>
        <h1 v-bind:class="[display ? 'yes' : 'no']" v-on:click="Active">
           <p>Home</p>
        </h1>
        <h1 v-bind:class="[display ? 'yes' : 'no']" v-on:click="Active">
           <p>Dashboard</p>
        </h1>
        <h1 v-bind:class="[display ? 'yes' : 'no']" v-on:click="Active">
           <p>new</p>
        </h1>
        <h1 v-bind:class="[display ? 'yes' : 'no']" v-on:click="Active">
           <p>This is active</p>
        </h1>
    </div>
</template>

<script>
export default {
    name:"Class",
 data()
{
    return {
       display:true  
    }
},
methods:
{
    Active()
    {
       
        this.display=!this.display;
    }
}
}

</script>

<style scoped>
.heading{
    color: orange;
}
.yes{
    color:green;
}
.no{
    color: orangered;
}
</style>