<template>
  <div class="wrapper">
    <img class="wrapper__img" src="http://www.dell-lee.com/imgs/vue3/user.png" alt="">
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="text" placeholder="请输入手机号">
    </div>
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="password" placeholder="请输入密码">
    </div>
    <div class="wrapper__login">登录</div>
    <div class="wrapper__register">立即注册</div>
  </div>
</template>

<script>
export default ({
  name: 'Login',
  setup () {

  }
})
</script>

<style lang="scss" scoped>
.wrapper {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  left: 0;
  right: 0;

  &__img {
    display: block;
    width: 0.66rem;
    height: 0.66rem;
    margin: 0 auto 0.4rem auto;
  }

  &__input {
    background: #F9F9F9;
    border: 1px solid rgba(0,0,0,0.10);
    border-radius: 6px;
    font-size: 0.16rem;
    color: #333333;
    height: 0.48rem;
    margin: 0 0.48rem 0.16rem 0.48rem;
    padding-left: 0.16rem;
    &__content {
      width: 100%;
      line-height: 0.48rem;
      border: none;
      outline: none;
      background: none;
    }
  }

  &__login {
    font-size: 16px;
    color: #FFFFFF;
    text-align: center;
    height: 0.48rem;
    background: #0091ff;
    margin: 0.12rem 0.48rem 0.16rem 0.48rem;
    border-radius: 0.04rem;
    line-height: 0.48rem;
  }

  &__register {
    font-size: 14px;
    color: rgba(0,0,0,0.50);
    text-align: center;
  }

}
</style>
