<template>
  <div class="toast">
    {{message}}}
  </div>
</template>

<script>
export default {
  props: [
    'message'
  ]
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
}
</style>
