<template>
  <div class="position">
      <span class="iconfont position__icon">&#xe619;</span>
        电子科技大学电子科技大学电子科技大学电子科技大学电子科技大学
        <span class="iconfont position__notice">&#xe60b;</span>
    </div>
    <div class="search">
      <img class="home_search_icon" src="../../assets/home_search.png" alt="">
      店铺优惠商品
    </div>
    <div class="banner">
      <img class="banner__img" src="http://www.dell-lee.com/imgs/vue3/banner.jpg" alt="">
    </div>

      <div class="icons">

        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/超市.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/菜市场.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/水果店.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/鲜花.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/医药健康.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/家居.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/蛋糕.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/签到.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/大牌免运.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="http://www.dell-lee.com/imgs/vue3/红包.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
      </div>
      <div class="gap"></div>
</template>

<script>
export default {
  name: 'StaticPart'
}
</script>

<style lang="scss">
@import '../../style/viriables.scss';
@import '../../style/mixins.scss';
.position {
  position: relative;
  padding: 0.16rem 0.24rem 0.16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipsis;
  .position__icon {
    position: relative;
    top: 0.01rem;
    font-size: 0.2rem;
  }
  .position__notice {
    right: 0;
    top: 0.17rem;
    position: absolute;
    font-size: 0.2rem;
  }
  color: $content-fontcolor;
}

.search {
  line-height: 0.32rem;
  background: #f5f5f5;
  color: #b7b7b7;
  border-radius: 0.16rem;
  font-size: 0.14rem;

}
.home_search_icon {
  position: relative;
  margin-left: 0.16rem;
  margin-top: -0.02rem;
  margin-right: 0.03rem;
  width: 0.16rem;
  height: 0.16rem;
  vertical-align: middle;
}

.banner {
  height: 0;
  overflow: hidden;
  padding-bottom: 25.4%;
  &__img {
    margin-top: 0.12rem;
    width: 100%;
  }
}

.icons{
  display: flex;
  flex-wrap: wrap;
  padding-top: 0.16rem;
  &__items {
    width: 20%;
    &__img {
      display: block;
      margin: 0 auto;
      width: 0.4rem;
      height: 0.4rem;
    }
    &__text {
      position: relative;
      margin-top: 0.06rem;
      text-align: center;
    }
  }
}

.gap {
  height: 0.1rem;
  margin: 0 -0.18rem;
  background: $content-bgColor;
}
</style>
