<template>
    <div class="top">
        <div class="top__header">
            <div class="top__header__back iconfont" @click="handleBackClick()">&#xe600;</div>
            确认订单
        </div>
        <div class="top__receiver">
            <div class="top__receiver__title">收货地址</div>
            <div class="top__receiver__address">广州</div>
            <div class="top__receiver__info">
                <span class="top__receiver__info__name">杨先生</span>
                <span class="top__receiver__info__name">123456789</span>
            </div>
            <div class="top__receiver__enter iconfont">&#xe8f1;</div>
        </div>
    </div>
</template>
<script>
import { useRouter } from 'vue-router'
export default {
  name: 'TopArea',
  setup () {
    const router = useRouter()
    const handleBackClick = () => { router.back() }
    return { handleBackClick }
  }
}
</script>

<style lang="scss" scoped>
@import '../../style/viriables.scss';
.top{
    position: relative;
    height: 1.96rem;
    background-size: 100% 1.59rem;
    background-image: linear-gradient(0deg, rgba(0,145,255,0.00) 4%, $btn-bgColor 50%);
    background-repeat: no-repeat;
    &__header {
        position: relative;
        padding-top: .26rem;
        line-height: .24rem;
        color: $bgColor;
        text-align: center;
        font-size: .16rem;
        &__back{
            position: absolute;
            left: .18rem;
            font-size: .22rem;
        }
    }
    &__receiver{
        position: absolute;
        left: .18rem;
        right: .18rem;
        bottom: 0;
        height: 1.11rem;
        background: $bgColor;
        border-radius: .04rem;
        &__title{
            line-height: .22rem;
            padding: .16rem 0 .14rem .16rem;
            font-size: .16rem;
            color: $content-fontcolor;
        }
        &__address{
            line-height: .2rem;
            padding: 0 .4rem 0 .16rem;
            color: $content-fontcolor;
            font-size: .14rem;
        }
        &__info{
            padding: .06rem 0 0 .16rem;
            &__name{
                margin-right: .06rem;
                line-height: .18rem;
                font-size: .12rem;
                color: #666;
            }
        }
        &__enter{
            position: absolute;
            right: .16rem;
            top: .5rem;
            color: #666;
            font-size: .2rem;
        }
    }
}
</style>
