<template>
    <section>
        <form @submit.prevent="setUserData">
         <div>
            <label>Name</label>
            <input type="name" v-model="enteredName "/>
         </div>
         <div>
            <label>Age</label>
            <input type="number" v-model="enteredAge"/>
         </div>
         <button>Set Data</button>
        </form>
    </section>
</template>


<script>
    export default{
        emits:['set-data'],
        data(){
            return{
                enteredName: '',
                enteredAge: ''
            }
        },
        methods:{
          setUserData(){
            this.$emit('set-data', this.enteredName, this.enteredAge)
          }  
        }
    }
</script>