<template>
    <div>
        <ol>
            <div v-for="(item,index) in this.dataList.quetitle" :key="index">
                <div>
                    {{item}}
                </div>
                <question/>
            </div>
            <button @click="makeSure">确认</button>
        </ol>
    </div>
</template>

<script>
import data from '@/components/data.js'
import question from '@/components/question.vue'

    export default {
        name:'quetitle',
        components:{
            question,
        },
        data(){
            return{
                dataList:data
            }
        },
        methods:{
            makeSure(){

            }
        }
        
    }
</script>

<style scoped>

</style>