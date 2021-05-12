<template>
  <div class="wrapper">
    <img class="wrapper__img" src="http://www.dell-lee.com/imgs/vue3/user.png" alt="">
    <div class="wrapper__input">
      <input v-model="data.username" class="wrapper__input__content" type="text" placeholder="请输入手机号">
    </div>
    <div class="wrapper__input">
      <input v-model="data.password" class="wrapper__input__content" type="password" placeholder="请输入密码">
    </div>
    <div class="wrapper__login" @click="handleLogin">登录</div>
    <div class="wrapper__register" @click="handleRegisterClick">立即注册</div>
    <Toast v-if="toastData.showToast" :message="toastData.toastMessage"/>
  </div>
</template>

<script>
import { useRouter } from 'vue-router'
import { reactive } from '@vue/reactivity'
import { post } from '../../utils/request'
import Toast, { userToastEffect } from '../../components/Toast'

export default ({
  name: 'Login',
  components: {
    Toast
  },
  setup () {
    const data = reactive({
      username: '111',
      password: '222'
    })
    const router = useRouter()

    const { showToast, toastData } = userToastEffect()

    const handleLogin = async () => {
      try {
        const result = await post('/api/user/login', {
          username: data.username,
          password: data.password
        })
        console.log(result)
        if (result?.errno === 0) {
          localStorage.isLogin = true
          router.push({ name: 'Home' })
        } else {
          showToast('登录失败')
        }
      } catch {
        showToast('请求失败')
      }
    }

    const handleRegisterClick = () => {
      router.push({ name: 'Register' })
    }
    return { handleLogin, handleRegisterClick, data, toastData }
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
