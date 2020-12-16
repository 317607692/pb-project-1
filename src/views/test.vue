<template>
    <div class="body">
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
        <!-- <div>
            <test :fuck="test()"></test>
        </div> -->
        <div class="wrapper">
            <el-tabs v-model="activeName" type="card" @tab-click="handleClick">
                <el-tab-pane label="官网资源（可联机，加载速度慢）" name="net">
                    <container>
                        <template>
                            <game type="net"></game>
                        </template>
                    </container>
                </el-tab-pane>
                <el-tab-pane
                    label="本服资源（不可联机可玩三方图，加载速度快）"
                    name="local"
                >
                    <container>
                        <template>
                            <game></game>
                        </template> </container
                ></el-tab-pane>
            </el-tabs>
        </div>
        <div class=wrapper>
            <el-progress
                :percentage="percentage"
                :color="customColor"
            ></el-progress>

            <el-progress
                :percentage="percentage"
                :color="customColorMethod"
            ></el-progress>

            <el-progress
                :percentage="percentage"
                :color="customColors"
            ></el-progress>
            <div>
                <el-button-group>
                    <el-button
                        icon="el-icon-minus"
                        @click="decrease"
                    ></el-button>
                    <el-button
                        icon="el-icon-plus"
                        @click="increase"
                    ></el-button>
                </el-button-group>
            </div>
        </div>

        <div class="wrapper">
            <!-- <game></game> -->
            <container titleText="这他喵是啥">
                <div class="github">
                    <a
                        class="href"
                        href="https://github.com/317607692/pb-project-1"
                    >
                        <span>欢迎来github查看本项目（点我进入）-by Luigi</span>
                    </a>
                </div>
            </container>
        </div>

        <!-- <div class="github">
            <a class="href" href="https://github.com/317607692/pb-project-1">
                <span>https://github.com/317607692/pb-project-1</span>
            </a>
        </div> -->
    </div>
</template>

<script>
import container from "@/components/container";
import test from "@/components/test-object";
import game from "@/components/game";
import Container from "../components/container.vue";
export default {
    data() {
        return {
            activeName: "net",
            form: {
                name: "",
                region: "",
                date1: "",
                date2: "",
                delivery: false,
                type: [],
                resource: "",
                desc: ""
            },
            rules: {
                name: [
                    {
                        required: true,
                        message: "请输入活动名称",
                        trigger: "blur"
                    },
                    {
                        min: 3,
                        max: 20,
                        message: "长度在 3 到 20 个字符",
                        trigger: "blur"
                    }
                ],
                region: [
                    {
                        required: true,
                        message: "请选择活动区域",
                        trigger: "change"
                    }
                ],
                date1: [
                    {
                        type: "date",
                        required: true,
                        message: "请选择日期",
                        trigger: "change"
                    }
                ],
                date2: [
                    {
                        type: "date",
                        required: true,
                        message: "请选择时间",
                        trigger: "change"
                    }
                ],
                type: [
                    {
                        type: "array",
                        required: true,
                        message: "请至少选择一个活动性质",
                        trigger: "change"
                    }
                ],
                resource: [
                    {
                        required: true,
                        message: "请选择活动资源",
                        trigger: "change"
                    }
                ],
                desc: [
                    {
                        required: true,
                        message: "请填写活动形式",
                        trigger: "blur"
                    }
                ]
            },
            percentage: 20,
            customColor: "#409eff",
            customColors: [
                { color: "#f56c6c", percentage: 20 },
                { color: "#e6a23c", percentage: 40 },
                { color: "#5cb87a", percentage: 60 },
                { color: "#1989fa", percentage: 80 },
                { color: "#6f7ad3", percentage: 100 }
            ]
        };
    },
    components: {
        test,
        game,
        container
    },
    methods: {
        customColorMethod(percentage) {
            if (percentage < 30) {
                return "#909399";
            } else if (percentage < 70) {
                return "#e6a23c";
            } else {
                return "#67c23a";
            }
        },
        increase() {
            this.percentage += 10;
            if (this.percentage > 100) {
                this.percentage = 100;
            }
        },
        decrease() {
            this.percentage -= 10;
            if (this.percentage < 0) {
                this.percentage = 0;
            }
        },
        test() {
            console.log("fuck: ");
        },
        submitForm(formName) {
            this.$refs[formName].validate(valid => {
                if (valid) {
                    alert("submit");
                } else {
                    alert("error");
                }
            });
        }
    }
};
</script>
<style lang="less" scoped>
// .container {
//     border: 1px solid #eee;
//     border-radius: 3px;
//     background: #fff;
// }
.wrapper {
    margin: 15px;
    &:first-child {
        margin-top: 0px;
    }
}
.github {
    width: auto;
    @height: 100px;
    height: @height;
    a.href {
        display: block;
        font-size: 14px;
        line-height: @height;
        height: @height;
        text-align: center;
        text-decoration: none;
        color: #fff;
        &:hover {
            // color: ;
        }
    }
}
</style>
