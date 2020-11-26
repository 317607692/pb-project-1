<template>
    <div class="game">
        <object width="800" height="400">
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
                    style="
                        display: block;
                        width: 800px;
                        height: 400px;
                        background-color: #050a22;
                        text-align: center;
                        font-width: normal;
                        color: #ffffff;
                        padding-top: 150px;
                        box-sizing: border-box;
                    "
                    >It looks like Flash Player which is required to play Plazma
                    Burst 2 is not installed in your browser.<br /><br />Click
                    here to visit Flash Player download page<br /><br /><img
                        src="https://www.adobe.com/images/shared/download_buttons/get_flash_player.gif"
                        alt="Get Adobe Flash player"
                    /><br /><br />
                    <div
                        style="
              color: #3c4882;
              text-align: center;
              margin-left: auto;
              margin-right: auto;F
              width: 400px;
            "
                    >
                        or you can download standalone version of a game by
                        clicking "Download / redistribute" at the bottom of this
                        page
                    </div></a
                ><!--[if !IE]>--></object
            ><!--<![endif]-->
        </object>
    </div>
</template>
<script>
export default {
    data() {
        return {};
    },
    props: {
        width: 800,
    },
};
</script>
<style lang="less" scoped>
.game {
    display: block;
    width: 800px;
    height: 400px;
}
</style>