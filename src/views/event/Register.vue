<template>
    <p>Register for the event here...</p>
    <button @click="register">Register me</button>
</template>
  
<script>
  export default {
    props: ['event'],
    methods: {
      register() {
        // call the API to register for the event
        this.$router.push({
          name: 'EventEdit',
          params: { id: this.event.id }
        })
      }
    }
  }
  </script>