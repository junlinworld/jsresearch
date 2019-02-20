<template>
    <div>
        <ol>
            <div v-for="(item,index) in this.dataList.questions" :key=index>
                <div>
                    {{item}}
                </div>
                <answerVue :msgAnswers=queanswers @sendBackAnswerList='handleSendBackAnswers'/>
            </div>
        </ol>
    </div>
</template>

<script>
    import data from '@/components/data.js'
    import answerVue from '@/components/answer.vue'

    export default {
        name:'question',
        components:{
            answerVue,
        },
        data(){
            return{
                dataList:data,
                queanswers:data.answers,
                answerGroup:[],
                
            }
        },
        methods:{
            handleSendBackAnswers(value){
                answerGroup.push(value);
            },
            sendBackAnswerGroup(){
                this.$emit('sendBackAnswerGroup',this.answerGroup);
            }
        },
        
    }
</script>

<style scoped>

</style>