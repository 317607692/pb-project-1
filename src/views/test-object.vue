<template>
    <div>
        <div class="fuck">
            <span>{{ text }}</span>
        </div>
    </div>
</template>
<script>
export default {
    name: "fuck",
    props: {
        text: {
            type: String,
            default: "fuck",
        },
    },
    data() {
        return {
            // content: this.text,
            contnet: "",
        };
    },
    methods: {
        init() {
            // this.content = this.text;
            console.log("txt: ", this.text);
        },
    },
    mounted() {
        this.init();
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
