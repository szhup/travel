<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
			<swiper-slide v-for="(item,index) in list" :key="index">
                <img class="swiper-img" :src="item.imgUrl" alt="">
            </swiper-slide>
			<div class="swiper-pagination" slot="pagination"></div>
		</swiper>
	</div>
</template>

<script type="text/ecmascript-6">
export default {
	name: "HomeSwiper",
	data() {
		return {
			swiperOption: {
				pagination : {
                    el:'.swiper-pagination'
                },
                loop:true
			}
		};
	},
	props:{
		list:{
			type:Array,
			required: true
		}
	}
};
</script>

<style scoped lang="stylus">
.wrapper /deep/ .swiper-pagination-bullet-active
    background: #fff
.wrapper {
	width: 100%;
	overflow: hidden;
	height: 0;
	padding-bottom: 31.5%;

	.swiper-img {
		width: 100%;
	}
}
</style>
