<script>
export default {
    name: "AppJumbo",
    data() {
        return {
            jumbo: "jumbotron.jpg"
        }
    },
    methods: {
        getImagePath(imagePath){
            return new URL(imagePath, import.meta.url).href;
        }
    }
}
</script>

<template>

    <section>
        <img :src="getImagePath(`../assets/${jumbo}`)">
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
section {
    height: 400px;
    img {
        height: 100%;
        width: 100%;
        object-fit: cover;
        object-position: 20% 0;
    }
}

</style>