<template>
    <div>
        <h3>{{title}}</h3>
        <p>{{context}}</p>
        <button @click="deleteT">删除该评论</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            
        }
    },
    props:['title','context','delteText','index'],
    created(){
        console.log("组件被创建")
    },
    methods:{
        deleteT(){
            // this.delteText(this.index)
            this.$emit('delteComment',this.index)
        }
    }
}
</script>

<style scoped>

</style>
