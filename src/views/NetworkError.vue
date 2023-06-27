<template>
    <div class="network-error">
        <h1>Network Error</h1>
        <p>Check your internet connection and 
            <a href="#" @click="$router.go(-1)">click here</a> to try again.</p>
    </div>
</template>