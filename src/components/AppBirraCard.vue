<script>
export default {
    name: "AppBirraCard",
    props: ["info"]
}
</script>

<template>
   <section class="container">
        <div>{{ info.id }}</div>

   </section>
</template>

<style scoped>

.container {
    width: 1100px;
    margin: 0 auto;
    display: flex;
}

</style>