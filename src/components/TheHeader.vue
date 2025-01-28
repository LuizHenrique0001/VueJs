<template>
    <header>
        <h1>Vue.js News</h1>
        <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
        </nav>
    </header>
</template>
<script>

export default {
    
}

</script>

<style scoped>
header {
    background-color: #bdbdbd;
    color: white;
    padding: 10px 0;
    text-align: center;
}
nav ul {
    list-style-type: none;
    display: flex;
    justify-content: space-around;

}
</style>