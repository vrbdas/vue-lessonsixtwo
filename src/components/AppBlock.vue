<script setup>

</script>

<template>
  <div class="card">
    <h3 class="title">
      <slot name="header"></slot>
    </h3>
    <slot name="default"></slot>
    <div class="footer" v-if="$slots.footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>


<style scoped lang='scss'>
.card {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  background-color: #ffffff;
  border-radius: 10px;
  padding: 20px;
}
.title {
  font-weight: 600;
}

.footer {
  color: darkgray;
}
</style>