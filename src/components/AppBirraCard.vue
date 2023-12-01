<script>
import { store } from '../store.js'
export default {
    name: "AppBirraCard",
    props: ["card"],
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container">
        <div v-if="store.searchStrings === '1'" class="beerMargin">
            <div>
                <h2>Nome della birra</h2>
                <h3 class="my"> {{ card.name }}</h3>
            </div>
        </div>

        <div v-if="store.searchStrings === '2'" class="beerMargin">
            <div>
                <h2>Città</h2>
                <p class="my">{{ card.city }}</p>
            </div>
        </div>

        <div v-if="store.searchStrings === '3'" class="beerMargin">
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
    margin: 20px 0;
    border: 1px solid red;
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