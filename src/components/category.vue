<template>
    <div>
        <ol>
            <div v-for="(item,index) in this.catagoryList" :key=index>
                <div>
                    {{catagoryList[index]}}
                </div>
                <div>
                    题目{{index}}
                </div>

            </div>
        </ol>
    </div>
</template>

<script>
    export default {
        name:'category',
        data(){
            return{
                catagoryList:['行为态度','工作品质','工作能力'],
            }
        },
        methods:{

        },
    }
</script>

<style scoped>

</style>