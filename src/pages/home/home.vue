<template>
    <div>
        <home-header></home-header>
        <home-swiper :list="swiperList"></home-swiper>
        <home-icons :list="iconList"></home-icons>
        <recommend :list="recommendList"></recommend>
        <home-weekend :list="weekendList"></home-weekend>
    </div>
</template>

<script type="text/ecmascript-6">
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
import recommend from './components/recommend'
import homeWeekend from './components/weekend'
import axios from 'axios'
export default {
    data() {
        return {
            swiperList:[],
            iconList:[],
            recommendList:[],
            weekendList:[]
        }
    },
    components:{
        HomeHeader,
        HomeSwiper,
        HomeIcons,
        recommend,
        homeWeekend
    },
    mounted:function(){
        this.getHomeInfo()
    },
    methods:{
        getHomeInfo(){
            axios.get('/api/index.json').then(res => {
                res = res.data
                if (res.ret && res.data) {
                    const data = res.data
                    this.swiperList = data.swiperList
                    this.iconList = data.iconList
                    this.recommendList = data.recommendList
                    this.weekendList = data.weekendList
                }
            })
        }
    }
}
</script>

<style scoped>
</style>
