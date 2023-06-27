<template>
    <div>
        <h1>404</h1>
        <p>The {{ resource }} you are looking for doesn't exist.</p>
        <router-link :to="{name: 'EventList'}">Go back to the list of events....</router-link>
    </div>
</template>
<script>
    export default {
        props: {
            resource: {
                type: String,
                required: true,
                default: 'page'
            }
        }
    }
</script>
