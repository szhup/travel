<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="(item,index) in recommendList" :key="index">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl">
                </div>
                <div class="item-info">
                    <p class="item-title" v-text="item.title"></p>
                    <p class="item-desc" v-text="item.desc"></p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script type="text/ecmascript-6">
export default {
    data() {
        return {
            recommendList:[{
                id:'0001',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                title:'京城周末撒欢',
                desc:'在帝都过周末，不仅仅是城中游！'
            },
            {
                id:'0002',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                title:'京城周末撒欢',
                desc:'在帝都过周末，不仅仅是城中游！'
            },{
                id:'0003',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
                title:'京城周末撒欢',
                desc:'在帝都过周末，不仅仅是城中游！'
            }]
        }
    },
}
</script>

<style scoped lang="stylus">
@import '~styles/mixins.styl'
    .title
        line-height .8rem
        background #eeeeee
        text-indent .2rem
    .item-img-wrapper
        overflow hidden
        height 0
        padding-bottom 33.9%
        .item-img
            width 100%
    .item-info
        padding .1rem
        .item-title
            line-height .54rem
            font-size .32rem
            ellipsis()
        .item-desc
            ellipsis()
            color #999
            line-height .4rem
</style>
