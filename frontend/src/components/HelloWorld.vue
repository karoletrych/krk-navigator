<template>
    <div>
        asdasd
        {{weather}}
    </div>
</template>

<script lang="ts">
import Vue from "vue";
import axios from "axios";

export default Vue.extend({
    name: "HelloWorld",
    async mounted() {
        // axios.defaults.baseURL = (config).VUE_APP_ENV_MyURL;
        axios.defaults.baseURL = "https://localhost:5001/";
        const w = await axios.get("weatherforecast");
        alert(w);
    },
    props: {}
});
</script>

<style scoped lang="scss"></style>
