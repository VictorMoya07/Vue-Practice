<template lang="html">
    <div >
    
    <ul class="color">
        <li v-for="user in users">
            {{user.name}} - {{user.Apellido}}
        </li>

    </ul>
     <form>

     </form>
    
    </div>
</template>


<script>
export default {
    data(){
        return{
            users: [
              {
                  name:'Jose',
                  Apellido:'Sanchez',
                  contac:false
              },
              {
                  name:'Jose',
                  Apellido:'Sanchez',
                  contac:false
              },  
              {
                  name:'Jose',
                  Apellido:'Sanchez',
                  contac:false
              }    
            ]
        }
    },
    methods:{
        addNewUser(){

        }
    }
}

</script>

<style media="screen">
    .color{
        background:brown;
        color:aliceblue;
    }
</style>

