<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <home-icons></home-icons>
    </div>
</template>

<script type="text/ecmascript-6">
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
export default {
    data() {
        return {
            
        }
    },
    components:{
        HomeHeader,
        HomeSwiper,
        HomeIcons
    },
}
</script>

<style scoped>
</style>
