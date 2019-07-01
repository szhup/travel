<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <div>{{obj[0]}}</div>
    </div>
</template>

<script type="text/ecmascript-6">
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
export default {
    data() {
        return {
            obj:[1,2]
        }
    },
    components:{
        HomeHeader,
        HomeSwiper
    },
    mounted:function(){
        this.$set(this.obj,0,9)
    }
}
</script>

<style scoped>
</style>
