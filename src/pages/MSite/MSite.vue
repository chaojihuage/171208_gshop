<template>
    <div class="msite">
        <!--首页头部-->
        <HeaderTop title="昌平区北七家宏福科技园(337省道北)">
            <span class="header_search" slot="left">
                <i class="iconfont icon-sousuo"></i>
            </span>
            <span class="header_login" slot="right">
                <span class="header_login_text">登录|注册</span>
            </span>
        </HeaderTop>
        <!--首页导航-->
        <nav class="msite_nav">
            <div class="swiper-container">
                <div class="swiper-wrapper">
                    <div class="swiper-slide">
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/001.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/002.png">
                            </div>
                            <span>商超便利</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/003.png">
                            </div>
                            <span>美食</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/004.png">
                            </div>
                            <span>简餐</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/005.png">
                            </div>
                            <span>新店特惠</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/006.png">
                            </div>
                            <span>准时达</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/007.png">
                            </div>
                            <span>预订早餐</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/008.png">
                            </div>
                            <span>土豪推荐</span>
                        </a>
                    </div>
                    <div class="swiper-slide">
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/009.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/010.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/010.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/010.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/010.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/010.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/010.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                        <a href="javascript:;" class="link_to_food">
                            <div class="food_container">
                                <img src="./images/nav/010.png">
                            </div>
                            <span>甜品饮品</span>
                        </a>
                    </div>
                </div>
                <div class="swiper-pagination"></div>
            </div>
        </nav>
        <!--首页附近商家-->
        <div class="msite_shop_list">
            <div class="shop_header">
                <i class="iconfont icon-catalog"></i>
                <span class="shop_header_title">附近商家</span>
            </div>
            <ShopList/>
        </div>
    </div>
</template>

<script>
    import Swiper from 'swiper'
    import 'swiper/dist/css/swiper.min.css'
    import HeaderTop from '../../components/HeaderTop/HeaderTop.vue'
    import ShopList from '../../components/ShopList/ShopList.vue'
    export default {
        components: {
            HeaderTop,
            ShopList
        },
        mounted () {
            // 创建一个Swiper实例对象，来实现轮播
            new Swiper('.swiper-container', {
                observer: true, // 修改swiper自己或子元素时，自动初始化swiper
                observeParents: true, // 修改swiper的父元素时，自动初始化swiper
                loop: true, // 可以循环轮播
                pagination: '.swiper-pagination',
                paginationClickable: true,
                paginationHide: false,
                speed: 1000, // 速度 越小越快
                autoplay: 5000 // 延迟 5秒
            })
        }
    }
</script>

<style lang="stylus" rel="stylesheet/stylus">
    @import "../../common/stylus/mixins.styl"
    .msite
        width 100%
        .header
            background-color #02a774
            position fixed
            z-index 100
            left 0
            top 0
            width 100%
            height 45px
            .header_search
                position absolute
                left 15px
                top 40%
                transform translateY(-50%)
                width 10%
                height 50%
                .icon-sousuo
                    font-size 25px
                    color #fff
            .header_title
                position absolute
                top 50%
                left 50%
                transform translate(-50%,-50%)
                width 50%
                color #fff
                text-align center
                .header_title_text
                    font-size 20px
                    color #fff
                    display block
            .header_login
                font-size 14PX
                color #fff
                position absolute
                right 15px
                top 50%
                transform translateY(-50%)
                .header_login_text
                    color #fff
        .msite_nav
            bottom-border-1px(#e4e4e4)
            margin-top 45px
            height 200px
            background #fff
            width 100%
            .swiper-container
                width 100%
                height 100%
                overflow auto
                .swiper-wrapper
                    display flex
                    flex-flow column wrap
                    .swiper-slide
                        display flex
                        flex-flow row wrap
                        >a
                            width 24.3%
                            margin-top 10px
                            text-align center
                            .food_container
                                img
                                    width 60%
                                span
                                    font-size 14px
                .swiper-pagination
                    .swiper-pagination-bullet-active
                        background-color: #52B54B
        .msite_shop_list
            overflow hidden
            top-border-1px(#e4e4e4)
            margin-top 10px
            background #fff
            z-index 200
            .shop_header
                padding 10px 10px 0
                .shop_icon
                    margin-left 5px
                    color #999
                .shop_header_title
                    color #999
                    font-size 14px
                    line-height 20px
</style>
