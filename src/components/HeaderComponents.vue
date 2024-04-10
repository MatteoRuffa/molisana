<template>
    <header class="container text-center ">
        <img src="../assets/img/la-molisana-logo.png" alt="logo">      
        <!-- <img src="/images/la-molisana-logo.png" alt="logo">        TRE MANIERE DI FARE LA STESSA COSA-->
        <!-- <img :src="'/images/' + img" alt="logo"> -->

        <ul>
            <li v-for="(item, index) in menu" :key="index">
                <a :href="item.url">{{ item.name }}</a>
            </li>
        </ul>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponents',
        data() {
            return {
                // img: 'la-molisana-logo.png'
                menu: [
                    {
                    name: 'home',
                    url: '#'
                    },
                    {
                    name: 'Prodotti',
                    url: '#'
                    },
                    {
                    name: 'Chi siamo',
                    url: '#'
                    },
                    {
                    name: 'Contatti',
                    url: '#'
                    }
                ],
            }
        },
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;

    header{
        ul{
            list-style: none;
            padding: 0;
            margin: 30px 0;
            display: flex;
            justify-content: center;

            li{
                margin: 0 10px;

                a{
                    text-decoration: none;
                    padding: 12px 18px;
                    color: black;
                    font-weight: 400;

                    &:hover {
                        background-color: $menuhover;
                    }
                }
            }
        }
    }
</style>