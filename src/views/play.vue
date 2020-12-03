<template>
    <div class="play">
        <div class="game">
            <game type="net"></game>
        </div>
    </div>
</template>
<script>
import game from "@/components/game";
import Game from '../components/game.vue';
export default {
    components: {
        game
    },
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
        width: 800px;
        height: 400px;
    }
}
</style>