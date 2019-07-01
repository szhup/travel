<template>
    <div class="header">
        <div class="header-left">
            <span class="iconfont">&#xe624</span>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632</span>
            输入城市游玩主题
        </div>
        <div class="header-right">
            城市<span class="iconfont">&#xe64a</span>
        </div>
    </div>
</template>

<script type="text/ecmascript-6">
export default {
    data() {
        return {

        }
    },
}
</script>
<style scoped lang="stylus">
    @import '~styles/varibles.styl';
    .header
        height: .86rem
        display flex
        justify-content space-between
        align-items center
        background: $bgColor
        color: #fff
        .header-left
            width: .64rem
            text-align center
            font-size .4rem
        .header-input
            height: .62rem
            flex:1
            border-radius .1rem
            background #fff
            margin-left .2rem
            color #ccc
            line-height .62rem
            padding-left .2rem
        .header-right
            width: 1.24rem
            text-align center
            span 
                font-size .24rem
</style>
