<template>
  <div class="wrapper">
    <img class="wrapper__img" src="http://www.dell-lee.com/imgs/vue3/user.png" alt="">
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="text" placeholder="请输入手机号">
    </div>
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="password" placeholder="请输入密码">
    </div>
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="password" placeholder="确认密码">
    </div>
    <div class="wrapper__register">注册</div>
    <div class="wrapper__login" @click="handleLoginClick">已有账号去登录</div>

  </div>
</template>

<script>
import { useRouter } from 'vue-router'
export default ({
  name: 'Register',
  setup () {
    const router = useRouter()
    const handleLoginClick = () => {
      router.push({ name: 'Login' })
    }
    return { handleLoginClick }
  }
})
</script>

<style lang="scss" scoped>
.wrapper {
  position: absolute;
  top: 20%;
  transform: translateY(-10%);
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

  &__register {
    font-size: 16px;
    color: #FFFFFF;
    text-align: center;
    height: 0.48rem;
    background: #0091ff;
    margin: 0.12rem 0.48rem 0.16rem 0.48rem;
    border-radius: 0.04rem;
    line-height: 0.48rem;
  }

  &__login {
    font-size: 14px;
    color: rgba(0,0,0,0.50);
    text-align: center;
  }

}
</style>
