<template>
    <div>
        <el-button type="primary" plain>fuck</el-button>
    </div>
</template>
<script>
export default {
    name: "fuck",
    methods:{
        innerMethod(val){
            console.log("here: ",val);
            this.$emit("fuck");
        }
    },
    mounted(){
        this.innerMethod(3);
    }
};
</script>