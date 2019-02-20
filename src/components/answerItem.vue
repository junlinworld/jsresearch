<template>
    <div>
        
        <div>
            <input v-model="inputData" type="text" @change="sendBackAnswer">
        </div>
    </div>
</template>

<script>
    export default {
        name:'answerItem',
        data(){
            return{
                inputData:'',
            }
        },
        methods:{
            sendBackAnswer(){
                this.$emit('sendBackAnswer',this.inputData);
            }
        }
    }
</script>

<style scoped>

</style>