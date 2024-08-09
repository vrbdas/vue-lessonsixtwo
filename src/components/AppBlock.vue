<script setup>
import { useSlots } from 'vue';

</script>

<template>
  <slot name="header"></slot>
  <slot>No text.</slot>
  <div class="footer" v-if="(useSlots()).footer">
    <slot name="footer"></slot>
  </div>
</template>


<style scoped lang='scss'>
$first: #fff;
$second: #FF9F1C;
$third: #FFBF69;
$fourth: #CBF3F0;
$fifth: #2EC4B6;

.footer {
  color: $fifth;
}
</style>