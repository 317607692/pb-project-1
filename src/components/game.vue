<template>
    <object class="game">
        <param
            name="movie"
            value="http://www.plazmaburst2.com/pb2/pb2_re34.swf?&amp;ver=1605515787&amp;l=&amp;p=&amp;a=&amp;default_server=0"
        />
        <param name="wmode" value="direct" />
        <param name="quality" value="high" />
        <param name="scale" value="default" />
        <param name="salign" value="lt" />
        <param name="allowScriptAccess" value="sameDomain" />
        <param name="allowFullScreen" value="true" />
        <param name="allowNetworking" value="all" />
        <param name="SeamlessTabbing" value="false" />
        <!--[if !IE]>-->
        <object
            type="application/x-shockwave-flash"
            data="pb2/pb2_re34.swf?&amp;ver=1605515787&amp;l=&amp;p=&amp;a=&amp;default_server=0"
            width="800"
            height="400"
            id="swfobj"
            style="outline: 0 !important"
        >
            <param
                name="movie"
                value="http://www.plazmaburst2.com/pb2/pb2_re34.swf?&amp;ver=1605515787&amp;l=&amp;p=&amp;a=&amp;default_server=0"
            />
            <param name="wmode" value="direct" />
            <param name="quality" value="high" />
            <param name="scale" value="default" />
            <param name="salign" value="lt" />
            <param name="allowScriptAccess" value="sameDomain" />
            <param name="allowFullScreen" value="true" />
            <param name="allowNetworking" value="all" />
            <param name="SeamlessTabbing" value="false" />
            <!--<![endif]-->
            <a
                target="_blank"
                href="http://www.adobe.com/go/getflash"
                class="hint"
            >
                <span>点我启动Flash player</span>
                <img
                    src="https://www.adobe.com/images/shared/download_buttons/get_flash_player.gif"
                />
                <div class="text-2">
                    or you can download standalone version of a game by clicking
                    "Download / redistribute" at the bottom of this page
                </div>
            </a>
            <!--[if !IE]>-->
        </object>
        <!--<![endif]-->
    </object>
</template>
<script>
export default {
    data() {
        return {
            gameUrl: "",
        };
    },
    props: {
        // width: 1200,
        // height: 400,
    },
};
</script>
<style lang="less" scoped>
.game {
    display: block;
    // width: 800px;
    // height: 400px;
    a.hint {
        display: block;
        width: 100%;
        height: 100%;
        background-color: #050a22;
        text-align: center;
        color: #ffffff;
        padding-top: 150px;
        box-sizing: border-box;
        text-decoration: none;
        .text-2 {
            color: #fff;
            text-align: center;
            margin-left: auto;
            margin-right: auto;
            width: 400px;
        }
    }
}
</style>