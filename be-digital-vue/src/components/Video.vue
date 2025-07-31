<template>
    <div class="maior">
        <div class="container-principal">
            <!-- Coluna do vídeo -->
            <div class="video-container-principal">
                <h2>Veja alguns dos nossos principais projetos:</h2>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/a4xCAJqrwoQ" title="Vídeo do YouTube"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen>
                    </iframe>
                </div>
            </div>

            <!-- Coluna do texto -->
            <div class="texto-container">
                <h3>Porque criamos isso?</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi dolore earum amet id distinctio
                    voluptates optio explicabo magnam veritatis cupiditate ratione a corrupti dicta, aspernatur
                    repudiandae, eum architecto repellendus nisi!</p>
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
.maior {
    min-height: 60vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1rem;
    box-sizing: border-box;
    background: #EEAECA;
    border-radius: 2rem;
    background: radial-gradient(circle, rgba(238, 174, 202, 1) 0%, rgba(148, 187, 233, 1) 100%);
}

.container-principal {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 4rem;
    max-width: 1200px;
    width: 100%;
}

.video-container-principal {
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.video-container {
    position: relative;
    padding-bottom: 56.25%;
    /* Proporção 16:9 */
    height: 0;
    overflow: hidden;
    width: 100%;
}

.video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: none;
}

.texto-container {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    max-width: 500px;
    padding: 2rem;
    border-radius: 2rem;
    border: solid 2px purple;
    background-color: rgba(255, 255, 255, 0.215);
}

h2 {
    font-weight: 800;
    font-size: 2.3rem;
    margin: 0;
    color: white;
    line-height: 2.5rem;
}

h3 {
    font-weight: 800;
    font-size: 1.9rem;
    margin: 0;
    text-align: center;
    color: aliceblue;
}

p {
    font-size: 1rem;
    line-height: 1.6;
    text-align: justify;
    color: aliceblue;
}
</style>
