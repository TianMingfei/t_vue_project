<template>
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
</template>

<script>
export default {
  name: 'Nearby'
}
</script>

<style lang="scss">
@import '../../style/viriables.scss';
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
