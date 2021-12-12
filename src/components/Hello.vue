<template>
  <div>
    <p>こんにちは、{{ name }}さん！！</p>
  </div>
</template>

<script>
export default {
  props: {
    name: String
  },
}
</script>

<style scoped>
p {
  font-size: x-large;
}
</style>