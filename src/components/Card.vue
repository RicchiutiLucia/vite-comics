<script>
export default {
    name: "Card",
    props: {
        thumb: Object
    }
}
</script>

<template>

    <div class="card">
        <div>
            <img :src="thumb.thumb" :alt="thumb.series">
        </div>
        <h6>{{ thumb.series.toUpperCase() }}</h6>
    </div>


</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 30px);
    margin: 20px 15px;
    h6{
        margin-top: 10px;
    }
}
</style>