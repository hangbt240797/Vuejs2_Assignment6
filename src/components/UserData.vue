<template>
    <section>
        <form @submit.prevent ="submitData">
            <label for="name">Your name:</label>
            <input type="text" placeholder="Enter Your Name here..." v-model="enterdName">
            <br>
            <br>
            <label for="age">Your age:</label>
            <input name="age" type="number" placeholder="Enter Your Age here..." v-model="enterdAge">
            <br>
            <br>
            <button>Set User Data</button>
        </form>        
    </section>
</template>
<script>
export default {
    emits:['set-data'],
    data(){
        return{
            enterdName: "",
            enterdAge: 0
        };
    },
    methods:{
        submitData(){
            this.$emit('set-data', this.enterdName, this.enterdAge);
        }
    }
}
</script>
