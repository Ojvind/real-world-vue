<script setup>
defineProps({
  event: {
    type: Object,
    required: true,
  }
})
</script>

<template>
  <RouterLink 
    :to="{ name: 'EventDetails', params: { id: event.id } }"
    class="event-link"
  >
    <div class="event-card">
      <h2>{{ event.title }}</h2>
      <span>@{{ event.time }} on {{ event.date }}</span>
    </div>
  </RouterLink>
</template>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}
 
.event-card:hover {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}
.event-link {
  text-decoration: none;
  color: inherit;
}
</style>
