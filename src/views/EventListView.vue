<script setup>
  import EventCard from '../components/EventCard.vue'
</script>

<template>
  <h1>öYeah Events App</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event"></EventCard>
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>



