<script>
import AppHeader from './components/AppHeader.vue'
import AppJumbo from './components/AppJumbo.vue'
import AppBirraCard from './components/AppBirraCard.vue'
import AppSearch from './components/AppSearch.vue'
import axios from 'axios'
import { store } from './store.js'

export default {
    components: {
        AppHeader,
        AppJumbo,
        AppBirraCard,
        AppSearch
    },
    data() {
        return {
            store
        }
    },
    mounted() {
        axios.get(this.store.apiUrl).then(result => {
            this.store.birre = result.data
        })
    }
}
</script>

<template>
    <AppHeader />
    <AppJumbo />
    <main>
        <AppSearch />
        <AppBirraCard v-for="element in store.birre" :card="element" />
    </main>
    <footer>

    </footer>
</template>

<style scoped></style>

getCharacters() {
    let indirizzo = this.store.apiUrl;

    if (this.store.searchString.length) {
        indirizzo += `?name=${this.store.searchString}`;
    }

    console.log("Richiama: ", indirizzo);

    axios.get(indirizzo).then(risultato => {
        // v. anche risultato.data.info 
        this.store.personaggi = risultato.data.results;
    })