<script>
export default {
    name: "AppHeader",
    data() {
        return {
            head: ["home", "chi siamo", "birrerie"]
        }
    }
}
</script>

<template>
    <section class="container">
        <h1>Logo</h1>
    <div>
        <a v-for="element in head" href="#">{{ element.toUpperCase() }}</a>
    </div>
    </section>
    
</template>

<style scoped>

.container {
    width: 1100px;
    margin: 20px auto;
    display: flex;
    justify-content: space-between;
}

a {
    margin-left: 16px;
    text-decoration: none;
    color: white;
}

</style>
