<template>
    <p>Register for the event here...</p>
    <button @click="register">Register me</button>
</template>
  
<script>
  export default {
    props: ['event'],
    inject: ['GStore'],
    methods: {
      register() {
        // call the API to register for the event
        this.GStore.flashMessage = 'You are sucessfully registered for ' + this.event.title

        setTimeout(() => {
          this.GStore.flashMessage = ''
        }, 3000)

        this.$router.push({
          name: 'EventDetails',
          params: { id: this.event.id }
        })
      }
    }
  }
  </script>