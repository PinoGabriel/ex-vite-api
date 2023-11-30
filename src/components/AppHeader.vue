<script>
export default {
    name: "AppHeader",
    data() {
        return {
            contacts: ["home", "chi siamo", "birrerie"]
        }
    }
}
</script>

<template>
    <section class="container">
        <img src="/img/logo.png" alt="logo">
    <div>
        <a v-for="element in contacts" href="#">{{ element.toUpperCase() }}</a>
    </div>
    </section>
    
</template>

<style scoped>

.container {
    width: 1100px;
    margin: 20px auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

a {
    margin-left: 16px;
    text-decoration: none;
    color: white;
    font-weight: 600;
}

img {
    width: 12%;
}

</style>
