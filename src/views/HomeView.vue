<script setup>
  import EventCard from '../components/EventCard.vue'
  import { ref } from 'vue'

  const events = ref([
    {
      id: 1,
      category: 'animal welfare',
      title: 'Pet Adoption Day',
      description: 'Find your new best friend',
      location: 'Seattle Central Library',
      date: '2021-07-04',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Seattle Animal Shelter',
    },
    {
      id: 1,
      category: 'animal welfare',
      title: 'Pet Adoption Day',
      description: 'Find your new best friend',
      location: 'Seattle Central Library',
      date: '2021-07-04',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Seattle Animal Shelter',
    },
    {
      id: 1,
      category: 'animal welfare',
      title: 'Pet Adoption Day',
      description: 'Find your new best friend',
      location: 'Seattle Central Library',
      date: '2021-07-04',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Seattle Animal Shelter',
    }
  ])
</script>

<template>
  <h1>Vue 3 Events App</h1>
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



