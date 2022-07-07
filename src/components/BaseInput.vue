<template>
  <label>{{label}}</label>
  <input
    :placeholder="label"
    :value="modelValue"
    v-bind="{
      ...$attrs,
      onInput: ($event) => {$emit('update:modelValue', $event.target.value)}
    }"
    class="field"
  >
</template>

<script>
export default {
  name: 'BaseInput',
  props: {
    label: {
      type: String,
      default: ''
    },
    modelValue: {
      type: [String, Number],
      default: ''
    }
  }
}
</script>

<style scoped>

</style>
