<template>
    <div class="body">
        <div class="github">
            <a class="href" href="https://github.com/317607692/pb-project-1">
                <span>https://github.com/317607692/pb-project-1</span>
            </a>
        </div>

        <!-- <el-form ref="form" :model="form" label-width="80px" :rules="rules">
            <el-form-item prop="name" label="姓名">
                <el-input
                    v-model="form.name"
                    placeholder="请输入内容"
                    clearable
                ></el-input>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="submitForm('form')">Submit</el-button>
            </el-form-item>
        </el-form> -->
        <div>
            <test></test>
        </div>
        <div>
            <!-- <game></game> -->
        </div>
    </div>
</template>

<script>
import test from "./test-object";
import game from "@/components/game";
export default {
    data() {
        return {
            form: {
                name: "",
                region: "",
                date1: "",
                date2: "",
                delivery: false,
                type: [],
                resource: "",
                desc: "",
            },
            rules: {
                name: [
                    {
                        required: true,
                        message: "请输入活动名称",
                        trigger: "blur",
                    },
                    {
                        min: 3,
                        max: 20,
                        message: "长度在 3 到 20 个字符",
                        trigger: "blur",
                    },
                ],
                region: [
                    {
                        required: true,
                        message: "请选择活动区域",
                        trigger: "change",
                    },
                ],
                date1: [
                    {
                        type: "date",
                        required: true,
                        message: "请选择日期",
                        trigger: "change",
                    },
                ],
                date2: [
                    {
                        type: "date",
                        required: true,
                        message: "请选择时间",
                        trigger: "change",
                    },
                ],
                type: [
                    {
                        type: "array",
                        required: true,
                        message: "请至少选择一个活动性质",
                        trigger: "change",
                    },
                ],
                resource: [
                    {
                        required: true,
                        message: "请选择活动资源",
                        trigger: "change",
                    },
                ],
                desc: [
                    {
                        required: true,
                        message: "请填写活动形式",
                        trigger: "blur",
                    },
                ],
            },
        };
    },
    components: {
        test,
        game,
    },
    methods: {
        submitForm(formName) {
            this.$refs[formName].validate((valid) => {
                if (valid) {
                    alert("submit");
                } else {
                    alert("error");
                }
            });
        },
    },
};
</script>
<style lang="less" scoped>
.container {
    border: 1px solid #eee;
    border-radius: 3px;
    background: #fff;
}
.github{
    width: auto;
    @height: 24px;
    a.href{
        display: block;
        font-size: 14px;
        line-height: @height;
        height: @height;
        text-align: center;
        text-decoration: none;
    }
}
</style>
