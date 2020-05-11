<template>
    <div class="header">
        <p>Current color: {{ bgColor }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            homeUrl: "http://localhost:8080/",
            offerUrl: "http://localhost:8080/offer",
            contactUrl: "http://localhost:8080/contact",
        }
    },
    props: ['bgColor']
}
</script>

<style scoped>

.header {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 10vh;
    background: transparent;
}

</style>