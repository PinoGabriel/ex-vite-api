<script>
import { store } from '../store.js'

export default {
    name: "AppSearch",
    data () {
        return {
            store
        }
    },
    methods: {
        io() {
            console.log(this.store.apiUrl);
        }
    }
}

</script>



<template>
    <div class="container">
        <select v-model="store.searchStrings" @change="io()">
            <option value="" disabled selected>Seleziona un'opzione</option>
            <option value="1">name</option>
            <option value="2">city</option>
            <option value="3">country</option>
            <option value="4">state_province</option>
        </select>
    </div>

</template>




<style scoped>
.container {
    width: 1100px;
    margin: 10px auto;
}
</style>