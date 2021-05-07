<template>
  <div class="wrapper">
    <div class="position">
      <span class="iconfont position__icon">&#xe619;</span>
        电子科技大学电子科技大学电子科技大学电子科技大学电子科技大学
        <span class="iconfont position__notice">&#xe60b;</span>
    </div>
    <div class="search">
      <img class="home_search_icon" src="./assets/home_search.png" alt="">
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
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
        <div class="icons__items">
          <img class="icons__items__img" src="./assets/logo.png" alt="">
          <p class="icons__items__text">账号</p>
        </div>
      </div>
      <div class="gap"></div>
      <div class="nearby">
        附近店铺
        <div class="nearby__item">
          <img class="nearby__item__img" src="http://www.dell-lee.com/imgs/vue3/near.png" alt="">
          <div class="nearby__content">
            <div class="nearby__content__title">
              山姆会员商店
            </div>
            <div class="nearby__content__tags">
              <span class="nearby__content_tag">
                月售1万加
              </span>
            </div>
            <div class="nearby__content__highlight">
              我是亮点我是亮点
            </div>
          </div>
        </div>

        <div class="nearby__item">
          <img class="nearby__item__img" src="http://www.dell-lee.com/imgs/vue3/near.png" alt="">
          <div class="nearby__content">
            <div class="nearby__content__title">
              山姆会员商店
            </div>
            <div class="nearby__content__tags">
              <span class="nearby__content_tag">
                月售1万加
              </span>
              <span class="nearby__content_tag">
                月售1万加
              </span>
              <span class="nearby__content_tag">
                月售1万加
              </span>
            </div>
            <div class="nearby__content__highlight">
              我是亮点我是亮点
            </div>
          </div>
        </div>

      </div>
  </div>
  <div class="docker">
    <span class="docker__item docker__item--active">
      <div class="iconfont">&#xe6f3;</div>
      <div class="docker__title">首页</div>
    </span>
    <span class="docker__item">
       <div class="iconfont">&#xe7e5;</div>
      <div class="docker__title">购物车</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe61e;</div>
      <div class="docker__title">订单</div>
    </span>
    <span class="docker__item">
      <div class="iconfont">&#xe660;</div>
      <div class="docker__title">我的</div>
    </span>

  </div>
</template>

<style lang="scss">
@import './style/viriables.scss';
@import './style/mixins.scss';
.docker {
  display: flex;
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  border-top: 1px solid $content-bgColor;
  padding: 0 0.18rem;
  box-sizing: border-box;
  color: $content-fontcolor;

  &__item {
    flex: 1;
    text-align: center;
    .iconfont {
      font-size: 0.2rem;
      margin: 0.07rem 0.02rem 0;
    }
    &--active {
      color: #1fa4fc;
    }
  }

  &__title {
    font-size: 20px;
    transform: scale(0.5, 0.5);
    transform-origin: center top;
  }
}

.wrapper {
  overflow-y: auto;
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0.5rem;
  right: 0;
  padding: 0 0.18rem 0.3rem 0.18rem;
}
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

.nearby {
  padding-top: 0.16rem;
  font-size: 0.18rem;
  color: $content-fontcolor;
  &__item {
    display: flex;
    padding-top: 0.12rem;
    &__img {
      margin-top: 0.12rem;
      width: 0.56rem;
      height: 0.56rem;
    }
  }

  &__content {
    flex: 1;
    padding-top: 0.12rem;
    margin-left: 0.16rem;
    border-bottom: 0.01rem solid $content-bgColor;
    padding-bottom: 0.12rem;
    &__title {
      color: $content-fontcolor;
      font-size: 0.16rem;
      line-height: 0.22rem;
    }
    &__tags {
      margin-top: 0.08rem;
      color: $content-fontcolor;
      font-size: 0.13rem;
      line-height: 0.18rem;
    }
    &__tag {
      margin-right: 0.16rem;
    }
    &__highlight {
      color: #e93b3b;
      font-size: 0.13rem;
      margin-top: 0.08rem;
    }

  }
}
</style>
