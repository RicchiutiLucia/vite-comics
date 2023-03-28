<script>
export default {
    name: "BlueSection",
    data() {
        return {
            items: [
                {
                    image: "buy-comics-digital-comics.png",
                    text: "DIGITAL COMICS",
                    url: "#"
                },
                {
                    image: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url: "#"
                },
                {
                    image: "buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url: "#"
                },
                {
                    image: "buy-comics-shop-locator.png",
                    text: "COMIC CHOP LOCATOR",
                    url: "#"
                },
                {
                    image: "buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url: "#"
                }
            ]
        }
    }
    ,
    methods: {
        getImagePath(imagePath){
            return new URL(imagePath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="merchandise">
        <ul class="container">
            <li v-for="item in items">
                <img :src="getImagePath(`../assets/${item.image}`)">
                <a :href="item.url">{{ item.text }}</a>
            </li>
        </ul>
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
.merchandise {
    background-color: $primary;
    height: 120px;
    .container {
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px;
        
        li {
            display: flex;
            align-items: center;
            padding: 10px;
            &:last-child img{
            height: 40px;
            }
            img {
            height: 50px;
            } 
        }
        a {
            padding-left: 10px;
            font-size: $font-medium;
            color: $text-white;
        }
        
        
    }
}
</style>