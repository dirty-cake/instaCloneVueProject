<template>
  <div class="input-container">
      <input
        class="input" 
        :placeholder="placeholder"
        :type="type"
      />
  </div>
    
</template>

<script>
export default {
  name: 'Input',
  props: {
    placeholder: { type: String, default: '' }, 
    type: { type: String, default: ''}
  }
}
</script>

<style scoped>

</style>
