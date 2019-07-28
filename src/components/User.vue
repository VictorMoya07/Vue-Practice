<template lang="html">
    <div >
    
    <ul class="color">
        <li v-for="user in users">
            {{user.name}} - {{user.Apellido}} 
            <button v-on:click="deleteUser(user)">X</button>
        </li>

    </ul>
     <form v-on:submit.prevent="addNewUser" >
       <input type="text" v-model ="newUser.name" placeholder="Agrege un Nombre" >
       <input type="text" v-model ="newUser.Apellido" placeholder="Agrege un Apellido" >
        <button type="submit">ADD</button>
     </form>
    
    </div>
</template>


<script>
export default {
    data(){
        return{
            users: [],
            newUser:{}
        }
    },
    methods:{
        addNewUser(){
          this.users.push(this.newUser);
          this.newUser = {};
        },
        deleteUser(user){
          this.users.splice(this.users.indexOf(user), 1);
        }
    },
    created(){
      this.$html.get('https://jsonplaceholder.typicode.com/users')
        .then(res => this.users = res.body);
    }
}

</script>

<style lang="css">
    .color{
        background:brown;
        color:aliceblue;
    }
</style>

