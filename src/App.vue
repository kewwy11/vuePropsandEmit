<template>
    <div>
      <active-user :userName="user.name" :userAge="user.age"></active-user>
      <user-data @set-data="newUserData"></user-data>
    </div>
</template>


<script>
    export default{
        data(){
            return{
                user:{
                    name: 'Erhis Grateful',
                    age: 19,
                }
            }
        },
        methods:{
            newUserData(name, age){
                this.user = {
                    name: name,
                    age: age
                }
            }
        }
    }
</script>

<style>
    html{
        font-family: sans-serif;
    }
    section {
        margin: 2rem auto;
        max-width: 40rem;
        border-radius: 12px;
        border: 2px solid green;
        padding: 1rem;
    }
</style>