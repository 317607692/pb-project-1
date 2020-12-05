<template>
    <div class="container">
        <div class="title">
            <span>{{ title }}</span>
        </div>
        <div class="content">
            <slot></slot>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        showTitle: {
            type: Boolean,
            default: true,
        },
        titleText: {
            type: String,
            default: "› Play Plazma Burst 2",
        },
    },

    data() {
        return {
            title: "",
        };
    },
    mounted() {
        this.title = this.titleText;
    },
};
</script>
<style lang="less" scoped>
.container {
    // margin: 15px;
    background-color: #252936;
    min-width: 10px;
    min-height: 10px;
    border-radius: 5px;
    overflow: hidden;
    .title {
        margin: 5px;
        background-color: #2c3442;
        position: relative;
        @height: 40px;
        height: @height;
        span {
            display: block;
            padding: 0px 10px 0px 10px;
            font-size: 15px;
            line-height: @height;
            height: @height;
            color: #fff;
        }
    }
    .content{
        min-height: 50px;
        background-color: #050A22;
        margin: 10px 15px 10px 15px;
    }
}
</style>