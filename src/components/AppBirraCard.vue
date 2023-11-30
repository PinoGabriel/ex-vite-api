<script>
export default {
    name: "AppBirraCard",
    props: ["card"]
}
</script>

<template>
    <div class="container">
        <div class="beerMargin">
            <div class="w-33">
                <h2>La Nostra Birra</h2>
                <h3 class="my"> {{ card.name }}</h3>
            </div>
            <div class="w-33">
                <h2>Ci trovi qui</h2>
                <p class="my">{{ card.city }}</p>
            </div>
            <div>
                <h2>Nazione di provenienza</h2>
                <p class="my">{{ card.country }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    width: 1100px;
    margin: 0 auto;
}

.beerMargin {
    margin: 20px;
    border: 1px solid red;
    display: flex;
    justify-content: space-between;
}

.w-33 {
    width: 33%;
}


h2 {
    color: red;
}

.my {
    margin: 10px 0;
}
</style>