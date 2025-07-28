<template>
       <nav>
         <img src="./icons/SER-DIGITAL.svg" alt="">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Sobre</a></li>
                <li><a href="#">Testemunhos</a></li>
                <li><a href="#">Contatos</a></li>
            </ul>
            </nav>
</template>
<script setup>
</script>
<style scoped>
ul{
    list-style: none;
    display: flex;
    justify-content: space-between;
}
li{

}
nav{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: var(--margin-nav);
    margin-bottom: var(--margin-nav);
}
</style>