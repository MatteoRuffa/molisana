<template>
    <div class="col-12 col-md-4">
        <h5>{{ title }}</h5>
        <ul>
            <li v-for="(item, index) in items" :key="index">
                <a :href="item.url">{{ item.name }}</a>
            </li>         
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'MenuComponents',
        props: ['title', 'items']   //QUELLO SOPRA FUNZIONA SOLO SE QUALCUNO GLI PASSA TITLE E ITEMS
    }
</script>

<style lang="scss" scoped>
    ul {
        list-style: none;
        padding: 0;

        a {
            text-decoration: none;
        }
    }
</style>