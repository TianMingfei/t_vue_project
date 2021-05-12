<template>
  <div class="toast">
    {{message}}
  </div>
</template>

<script>
import { reactive, toRefs } from '@vue/reactivity'
export default {
  props: [
    'message'
  ]
}

export const userToastEffect = () => {
  const toastData = reactive({
    show: false,
    toastMessage: ''
  })

  const showToast = (message) => {
    toastData.show = true
    toastData.toastMessage = message
    setTimeout(() => {
      toastData.show = false
      toastData.toastMessage = ''
    }, 2000)
  }

  const { show, toastMessage } = toRefs(toastData)

  return { showToast, show, toastMessage }
}

</script>

<style lang="scss" scoped>
.toast {
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  background: rgba($color: #000000, $alpha: 0.35);
  border-radius: 0.05rem;
  padding: 0.1rem;
  color: white;
}
</style>
