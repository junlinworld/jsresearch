<template>
    <div>
        <ol>
            <div class="answer" v-for="(item,index) in this.msgAnswers" :key=index>
                <div class="item">
                    {{item}}
                    <answerItem @sendBackAnswer='handleSendBackAnswer' />
                </div>
                <!-- <input v-model="inputData[index]" type="text"> -->
                
            </div>
            
                
            
        </ol>
    </div>
</template>

<script>
import answerItem from '@/components/answerItem.vue'
    export default {
        name:'answer',
        components:{
            answerItem,
        },
        props:{
            msgAnswers:Array,
        },
        data(){
            return{
                
                answerList:[],
            }
        },
        methods:{
            handleSendBackAnswer(value){
                answerList.push(value);
            },
            sendBackAnswerList(){
                if(answerList.length == 5){
                    this.$emit('sendBackAnswerList',this.answerList);
                }
            }
        },
        mounted:function(){
            this.sendBackAnswerList();
        }
    }
</script>

<style scoped>
    .item{
        display: inline
    }

    
</style>