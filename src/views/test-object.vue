<template>
    <div>
        <div class="fuck"><span>fuck</span></div>
    </div>
</template>
<script>
export default {
    name: "fuck",
    props: {
        text: String,
        default: "fuck",
    },
};
</script>

<style lang="less">
.fuck {
    display: block;
    text-align: center;
    span {
        font-size: 20px;
        line-height: 100px;
    }
}
</style>
