<script setup lang="ts">
import { ref } from 'vue'
import Event from '@/types/Event'
defineProps<{
  event: Event
}>()
</script>

<template>
  <div class="category">
    <div class="category-card">
      <span>{{ event.category }}</span>
      <span>{{ event.organizer }}</span>
    </div>
  </div>
</template>

<style scoped>
.category-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
  display: flex;
  justify-content: flex-end;
  font-size: 16px;
  text-align: right;
}

.category-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}

.category span {
  margin-left: 10px;
}
</style>
