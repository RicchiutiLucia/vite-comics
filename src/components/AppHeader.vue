<script>
export default {
    name: "AppHeader",
    data() {
        return {
            logo: "dc-logo.png",
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false
                },
            ]
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
    <header>
        <div class="container">
            <a href="#">
                <img :src="getImagePath(`../assets/${logo}`)">
            </a>
            <nav>
                <ul>
                    <li v-for="link in links"><a href="#">{{ link.text }}</a></li>
                </ul>
            </nav>
        </div>


    </header>


</template>

<style  lang="scss" scoped>
@use "../styles/partials/variables" as *;



header {
    height: 90px;
    padding: 10px 0;
    .container{
        display: flex;
        justify-content: space-between;
        align-content: center;
        align-items: center;
    }
    img {
        height: 65px;
    }
    ul {
        display: flex;
        li a {
            padding: 0 10px;
            font-size: $font-medium;
            color: $text-nav;
            &:hover {
                border-bottom: 3px solid #0282f9;
            }
        }
    }
}
</style>
