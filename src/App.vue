<script >
import AppHeader from './components/AppHeader.vue'
import AppJumbo from './components/AppJumbo.vue'
import AppBirraCard from './components/AppBirraCard.vue'
import axios from 'axios'
import { store } from './store.js'

export default {
    components: {
        AppHeader,
        AppJumbo,
        AppBirraCard
    },
    data() {
        return {
            store
        }
    }, 
    mounted() {
        axios.get(this.store.apiUrl).then(result=> {
            this.store.birre = result.data
        })
    }
}
</script>

<template>
    <AppHeader />
    <AppJumbo />
    <main>
        <AppBirraCard v-for="element in store.birre" :info="element"/>
    </main>
    <footer>

    </footer>
</template>

<style scoped></style>
