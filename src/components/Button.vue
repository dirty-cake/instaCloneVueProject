<template>
  <button class="button" v-bind="$attrs"><slot/></button>
</template>

<script>
export default {
  name: 'Button',
  props: {}
}
</script>

<style lang="scss" scoped>
.button {
  width: 100%;
  border: none;
  padding: 10px 0;
  font-size: 16px;
  border-radius: 5px;
  outline: none;
  cursor: pointer;
  background-color: #0095f6;
  color: #FFFFFF;
  &:disabled {
    opacity: 0.4;
    cursor: not-allowed;
  }
}
</style>
