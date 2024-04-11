<template>
    <main>
        <div class="container py-4">
            <h2>Lista Prodotti</h2>
            <div class="row">
                <div class="col-12 col-md-6 col-lg-3 mb-4" v-for="(item, index) in products" :key="index">
                    <CardComponent :image="item.src" :title="item.titolo" :text="`Tipo: ${item.tipo} - Cottura: ${item.cottura}`" @elimina="removePasta(index)"/>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import CardComponent from './CardComponent.vue';
import { prodotti } from '../data/store.js';
    export default {
        name: 'MainComponents',
        components: {
            CardComponent
        },
        data () {
            return {
                products: prodotti,
            }
        },
        methods: {
            removePasta(index) {
                this.products.splice(index, 1);
            }
        },
        mounted() {
            console.log(this.products);
        }
    }
</script>

<style lang="scss" scoped>
    main {
        background-image: url('../assets/img/fondo-pag-speciali.jpg');
        h2{
            color: blue;
            text-align: center;
        }
    }
</style>