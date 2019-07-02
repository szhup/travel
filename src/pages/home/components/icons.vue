<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page,index) in pages" :key="index">
                <div class="icon" v-for="(icon,iconIndex) in page" :key="iconIndex">
                    <img class="icon-img" :src="icon.url">
                    <p v-text="icon.desc"></p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script type="text/ecmascript-6">
export default {
    name:'HomeIcons',
    data() {
        return {
            iconList:[
                {
                    id:'0001',
                    url:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                    desc:"热门景点"
                },
                {
                    id:'0002',
                    url:'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
                    desc:"热门景点"
                },
                {
                    id:'0003',
                    url:'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                    desc:"热门景点"
                },
                {
                    id:'0004',
                    url:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/338c5b924c5809e8c7b14f60a953c3e2.png',
                    desc:"热门景点"  
                },
                {
                    id:'0005',
                    url:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                    desc:"热门景点"
                },
                {
                    id:'0006',
                    url:'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
                    desc:"热门景点"
                },
                {
                    id:'0007',
                    url:'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                    desc:"热门景点"
                },
                {
                    id:'0008',
                    url:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/338c5b924c5809e8c7b14f60a953c3e2.png',
                    desc:"热门景点"
                },
                {
                    id:'0009',
                    url:'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                    desc:"热门景点"
                }
            ]
        }
    },
    computed:{
        pages(){
            let pages = []
            this.iconList.forEach((item,index) => {
                let page = Math.floor(index/8)
                if(!pages[page]){
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>

<style scoped lang="stylus">
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
    .icons >>> .swiper-container
        height 0
        overflow hidden
        padding-bottom 50%
    .icon
        float left
        width 25%
        text-align center
        padding 0 .22rem
        .icon-img{
            width 100%
        }
        p
            line-height .44rem
            color $darkTextColor
            ellipsis()
</style>
