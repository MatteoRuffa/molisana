<template> 
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-12 col-md-4"><img src="../assets/img/la-molisana-logo.png" alt="logo"></div>
                <MenuComponents title="Prodotti" :items="links.Prodotti"/>
                <MenuComponents title="Pastificio" :items="links.Pastificio"/>
                <!-- <div class="col-12 col-md-4">      PROVA SENZA FARE UN COMPONENTE
                    <h5>Prodotti</h5>
                    <ul>
                        <li v-for="(item, index) in Prodotti" :key="index">
                            <a :href="item.url">{{ item.name }}</a>
                        </li>           
                    </ul>
                </div> -->
                <!-- <div class="col-12 col-md-4">
                    <h5>Pastificio</h5>
                    <ul>

                    </ul>
                </div> -->  
            </div>
        </div>
    </footer>
</template>

<script>
    import MenuComponents from './MenuComponents.vue'; 
    export default {
        name: 'FooterComponents',
        data() {
            return {
                links: {
                    Prodotti: [
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
                    Pastificio: [
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
                },
            }
        }
    }
</script>

<style lang="scss" scoped>
    footer {
        background-image: url('../assets/img/footer-montagne-bottom.jpg');
        background-position: bottom;
        background-repeat: no-repeat;
    }
</style>