<script setup>
  import EventCard from '../components/EventCard.vue'
  import { ref } from 'vue'

  const events = ref([
    {
      id: 1,
      category: 'altnernative',
      title: 'God Save the Queen',
      description: 'old-school british punk',
      location: 'Soho, London',
      date: '2021-07-04',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Three Cord Records',
    },
    {
      id: 1,
      category: 'black metal',
      title: 'Troll Metal Fest',
      description: 'Enjoy the best of the best in troll metal',
      location: 'Hammerfest, Norway',
      date: '2021-07-04',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Lucifer Records',
    },
    {
      id: 1,
      category: 'metal',
      title: 'Swallow the Sun',
      description: 'Finish doom metal',
      location: 'Helsinki, Finland',
      date: '2021-07-04',
      time: '12:00',
      petsAllowed: true,
      organizer: 'Metal maniacs',
    }
  ])
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



