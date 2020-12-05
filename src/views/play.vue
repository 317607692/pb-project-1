<template>
    <div class="play">
        <div class="game">
            <game ref="game" type="local"></game>
        </div>
        <a href="javascript:;" class="btn" @click="test()">
            <span>click</span>
        </a>
    </div>
</template>
<script>
import game from "@/components/game";
import Game from '../components/game.vue';
export default {
    components: {
        game
    },
    methods:{
        test(){
            console.log(this.$refs.game);
        }
    }
}
</script>
<style lang="less" scoped>
.play{
    width: auto;
    height: auto;
    position: relative;
    .game{
        position: relative;
        margin: 0 auto;
        @width: 900px;
        width: @width;
        height: @width/2;
    }
    .btn{
        display: block;
        width: 100px;
        height: 30px;
        background-color: #eee;
        span{
            display: block;
            line-height: 30px;
        }
    }
}
</style>