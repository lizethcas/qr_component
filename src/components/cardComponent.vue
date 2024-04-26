<template>
    <article class="card">
        <div class="qr_container">
            <img src="../assets/qr.png" alt="QR" class="qr">
        </div>
        <div class="container_description">
            <h2 class="title">{{ infoCard.title }}</h2>
            <p class="description">{{ infoCard.description }}</p>
        </div>
    </article>
</template>

<script setup lang="ts">
interface INFO {
    title: string,
    description: string
}


const infoCard: INFO = {
    title: "Improve your front-end skills by building projects",
    description: "Scan the QR code to visit Frontend Mentor and take your coding skills to the next level"
}
</script>

<style scoped>
.container_description {
    margin: auto;
    max-width: 288px;
    width: 90%;
}

.qr_container {
    background-color: #3685FF;
    max-width: 288px;
    height: 288px;
    margin: auto;
    border-radius: 8px;
    overflow: hidden;
    position: relative;
}

.qr_container::after,
.qr_container::before {

    content: '';
    /* Añade contenido a los pseudo-elementos */
    position: absolute;
    /* Establece posición absoluta para posicionarlos correctamente */
    width: 270px;
    /* Ancho de los semicírculos */
    height: 270px;
    /* Altura de los semicírculos */
    background-color: #f2f2f213;
    /* Color de fondo de los semicírculos */
    border-radius: 50%;
    /* Hace que los elementos sean semicírculos */
}

.qr_container::after {
    bottom: -158px;
    right: -115px;
}

.qr_container::before {
    top: -147px;
    left: -113px;
}

.qr {
    padding: 64px;

}

.card {
    margin: auto;
    max-width: 320px;
    background-color: #FFFFFF;
    border-radius: 20px;
    height: 497px;
}

.description,
.title{
    font-family: "Outfit", sans-serif;
}


.title {
    color: #1F314F;
    font-size: 22px;
    font-weight: 700;
}

.description {
    color: #7D889E;
    font-size: 15px;
    font-weight: 400;
    text-align: center
}
</style>