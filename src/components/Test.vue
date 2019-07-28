<template>
    <div>
    <h1>{{user.firstName}}</h1>
    <input type="text" v-model="user.firstName">
    <button type ="button" v-on:click="saludar(user.firstName)">Hey haz click aca</button> 
    </div>
</template>


<script>
export default {
    data(){
        return{
            title:'Hola Vuejjs',
            user:{
                firstName:'Pedro',
                lastName:'McMillan'
            },
            myhtml:'<h1>hola PAPA</h1>'
        }
    },
        methods:{
    saludar(name){
        alert('hello'+ name)
    }
}
}

</script>

<style media="screen">

</style>


