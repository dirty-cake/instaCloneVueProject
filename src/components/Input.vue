<template>
  <div class="input-container">
    <input class="input" v-bind="$attrs" v-model="value" />
  </div>
</template>

<script>
import { computed } from 'vue'
export default {
  name: 'Input',
  props: {
    modelValue: {
      type: String, 
      default: ''
    }
  },
  emits: ['update:modelValue'],
  setup(props, context) {
    const value = computed({
      get: () => props.modelValue,
      set: value => context.emit('update:modelValue', value)
    })
    return {
      value
    }
  }
}
</script>

<style scoped>
.input {
  background: #fafafa;
  outline: none;
  border: 1px solid #dbdbdb;
  font-size: 16px;
  padding: 10px 0 7px 8px;
  border-radius: 5px;
  width: 100%;
  box-sizing: border-box;

}
</style>
