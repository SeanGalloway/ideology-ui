<template>
<div class="block">
  <label>{{ label }}:</label>
  <input :id=label
         :type=type
         v-bind:value="value"
         v-on:input="$emit('input', $event.target.value)"
  />
</div>
</template>

<script>
export default {
  name: "LabeledInput",
  props: {
    label: String,
    type: String,
    value: String
  }
}
</script>

<style scoped>

</style>