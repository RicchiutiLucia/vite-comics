<script>
import Card from './Card.vue';
export default {
    name: "AppMain",
    components:{
        Card
    },
    data() {
        return {
            cards:[
                        {
                            "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$19.99",
                            "series": "Action Comics",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                            "price": "$3.99",
                            "series": "American Vampire 1976",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
                            "price": "$16.99",
                            "series": "Aquaman",
                            "type": "graphic novel"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$2.99",
                            "series": "Batgirl",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640", 
                            "price": "$3.99",
                            "series": "Batman",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                            "price": "$2.99",
                            "series": "Batman Beyond",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                            "price": "$3.99",
                            "series": "Batman/Superman",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                            "price": "$4.99",
                            "series": "Batman/Superman Annual",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
                            "price": "$5.99",
                            "series": "Batman: The Joker War Zone",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                            "price": "$6.99",
                            "series": "Batman: Three Jokers",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$4.99",
                            "series": "Batman: White Knight Presents: Harley Quinn",
                            "type": "comic book"
                        },
                        {
                            "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                            "price": "$16.99",
                            "series": "Catwoman",
                            "type": "graphic novel"
                        }
                        ]
        }
    }
}
</script>

<template>
    
    <main>
        <div class="container">

            <a href="#" class="button current">CURRENT SERIES</a>

            <div class="cards">
                <Card v-for="card in cards" :thumb="card" />
            </div>

            <a href="#" class="button load">LOAD MORE</a>

        </div>
    </main>

</template>

<style lang="scss" scoped>

@use "../styles/partials/variables" as *;
main {
    background-color: #1c1c1c;
    .container {
        color: $text-white;
        text-align: center;
        padding: 30px 0;
        position: relative;
        .cards {
            display: flex;
            flex-wrap: wrap;
            margin-inline: -15px;
        }
        .button {
            display: inline-block;
            color: $text-white;
            background-color: $primary;
            font-weight: bolder;
            margin-top: 20px;
            &.current {
                padding: 10px 20px;
                position: absolute;
                left: 0;
                top: -40px;
            }
            &.load {
                padding: 10px 40px;
            }
        }
    }
}

</style>