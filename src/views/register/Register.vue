<template>
  <div class="wrapper">
    <img class="wrapper__img" src="http://www.dell-lee.com/imgs/vue3/user.png" alt="">
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="text" placeholder="请输入手机号" v-model="username">
    </div>
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="password" placeholder="请输入密码" v-model="password">
    </div>
    <div class="wrapper__input">
      <input class="wrapper__input__content" type="password" placeholder="确认密码" v-model="ensurement">
    </div>
    <div @click="handleRegister" class="wrapper__register">注册</div>
    <div class="wrapper__login" @click="handleLoginClick">已有账号去登录</div>
    <Toast v-if="show" :message="toastMessage"/>
  </div>
</template>

<script>
import { useRouter } from 'vue-router'
import { reactive, toRefs } from '@vue/reactivity'
import { post } from '../../utils/request'
import Toast, { userToastEffect } from '../../components/Toast'

const useRegisterEffect = (showToast) => {
  const router = useRouter()
  const data = reactive({
    username: '111',
    password: '222',
    ensurement: '444'
  })
  const handleRegister = async () => {
    try {
      const result = await post('/api/user/register', {
        username: data.username,
        password: data.password
      })
      console.log(result)
      if (result?.errno === 0) {
        router.push({ name: 'Login' })
      } else {
        showToast('注册失败')
      }
    } catch {
      showToast('请求失败')
    }
  }
  const { username, password, ensurement } = toRefs(data)

  return { username, password, handleRegister, ensurement }
}

const useLoginEffect = () => {
  const router = useRouter()
  const handleLoginClick = () => {
    router.push({ name: 'Login' })
  }
  return { handleLoginClick }
}

export default ({
  name: 'Register',
  components: {
    Toast
  },
  setup () {
    const { handleLoginClick } = useLoginEffect()
    const { showToast, show, toastMessage } = userToastEffect()
    const { username, password, handleRegister, ensurement } = useRegisterEffect(showToast)

    return { handleLoginClick, show, toastMessage, username, password, handleRegister, ensurement }
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
