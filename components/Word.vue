<template>
    <nuxt-link :to="'/words/' + id">
        <article class="word">
            <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail +')'}"></div>
            <h1>{{ word }}</h1>
            <p>{{ description }}</p>
        </article>
    </nuxt-link>
</template>

<script>
export default {
    props: [
        'thumbnail',
        'word',
        'description',
        'id'
    ]
}
</script>

<style scoped>
a {
    text-decoration: none;
    color: black;
}
a:hover {
    color: #666;
}
.word {
    box-sizing:border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #aaa;
    margin: 10px;
}

.thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
}
</style>