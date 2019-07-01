<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
			<swiper-slide>
                <img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/5187ef5a133b3aab0e0d90bd1df5cd02.jpg_750x200_3cd41f2b.jpg" alt="">
            </swiper-slide>
            <swiper-slide>
                <img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/818f6cc784ae6669b74bbbb255414a53.jpg_750x200_66ca5873.jpg" alt="">
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
	padding-bottom: 26.67%;

	.swiper-img {
		width: 100%;
	}
}
</style>
