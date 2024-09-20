<script setup>

</script>

<template>
  <div class="card">
    <ul>
      <li v-for="(item, i) in ['zero', 'one', 'two', 'three']">
        <slot :iter="item" :idx="i"></slot>
      </li>
    </ul>
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
</style>