<script setup>
import { ref, onMounted } from 'vue';

export default {
  name: 'Canvas',
  setup() {
    const canvas = ref(null);

    onMounted(() => {
      const ctx = canvas.value.getContext('2d');
      ctx.fillStyle = 'red';
      ctx.fillRect(0, 0, 200, 200);
    });

    return {
      canvas,
    };
  },
};

</script>

<template>
  <canvas ref="canvas" width="200" height="200"></canvas>
</template>

<style scoped>

</style>