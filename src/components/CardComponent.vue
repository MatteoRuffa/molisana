<template>
     <div class="card" style="width: 18rem;">
        <img :src="image" class="card-img-top" :alt="title">
        <div class="card-body">
            <h5 class="card-title">{{title}}</h5>
            <p class="card-text">{{text}}</p>
            <a href="#" class="btn btn-danger" @click="$emit('elimina')">Remuve</a>
     </div>
</div>
</template>

<script>
    export default {
        name: 'CardComponent',
        props: ['image', 'title', 'text', 'link']
    }
</script>

<style lang="scss" scoped>

</style>