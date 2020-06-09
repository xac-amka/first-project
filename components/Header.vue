<template>
    <header>
        <nav>
            <ul>
                <li><nuxt-link to="/">Starting page</nuxt-link></li>
                <li><nuxt-link to="/words">Words</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>
<script>
export default {
    data(){
        return {
            activeClass: 'active'
        }
    }
}
</script>
<style scoped>

li.active {
    font-weight: 700;
    font-size: larger;
}
a {
    text-decoration: none;
    color: white;
}
a:hover {
    color: #999;
}
header {
    width: 100%;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: black;
}

ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
}

li {
    margin: 0 10px;
}
</style>