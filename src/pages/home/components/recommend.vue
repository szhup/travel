<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="(item,index) in recommendList" :key="index">
                <img class="item-img" :src="item.imgUrl">
                <div class="item-info">
                    <p class="item-title" v-text="item.title"></p>
                    <p class="item-desc" v-text="item.desc"></p>
                    <button class="item-button">查看详情</button>
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
                imgUrl:'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
                title:'京城周末撒欢',
                desc:'在帝都过周末，不仅仅是城中游！'
            },
            {
                id:'0002',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
                title:'京城周末撒欢',
                desc:'在帝都过周末，不仅仅是城中游！'
            },{
                id:'0003',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
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
        margin-top .2rem
        line-height .8rem
        background #eeeeee
        text-indent .2rem
    .item
        display flex
        height 1.9rem
        overflow hidden
        .item-img
            width 1.7rem
            height 1.7rem
            padding .1rem
        .item-info
            flex 1
            padding .1rem
            min-width 0
            .item-title
                line-height .54rem
                font-size .32rem
            .item-desc
                ellipsis()
                line-height .4rem
                color #999
                ellipsis()
            .item-button
                background #ff9300
                padding 0 .1rem
                border-radius .06rem
                margin-top .16rem
                line-height .44rem
</style>
