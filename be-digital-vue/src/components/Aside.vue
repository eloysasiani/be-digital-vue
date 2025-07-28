<template>
    <h2>O que nossos clientes nos dizem:</h2>
    <div class="col1">
        <div class="col_card">
            <img :src="westernMan1" alt="">
            <span>Andrew Rathore</span>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ullamcorper scelerisque mi, in malesuada
                felis malesuada vel. </p>
        </div>
        <div class="col_card">
            <img :src="westernMan2" alt="">
            <span>Vera Duncan</span>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ullamcorper scelerisque mi, in malesuada
                felis malesuada vel. </p>
        </div>
        <div class="col_card">
            <img :src="westernMan3" alt="">
            <span>Mark Smith</span>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ullamcorper scelerisque mi, in malesuada
                felis malesuada vel. </p>
        </div>
    </div>

</template>
<script setup>
import westernMan1 from "@/assets/images/western-man-4975942-4159828-1-2x.png"
import westernMan2 from "@/assets/images/western-man-4975942-4159828-2-2x.png"
import westernMan3 from "@/assets/images/western-man-4975942-4159828-3-2x.png"
</script>
<style scoped></style>