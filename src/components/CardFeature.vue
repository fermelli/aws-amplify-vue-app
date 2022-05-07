<script>
export default {
    name: 'CardFeature',
    props: {
        feature: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
    <div class="card">
        <div class="card__container-image">
            <img class="card__image" :src="`./src/assets/${feature.image.src}`" :alt="feature.image.alt">
        </div>
        <h2 class="card__title">{{ feature.title }} ({{ feature.count }})</h2>
        <button class="card__button" @click="$emit('add-to-count')">Vote!</button>
    </div>
</template>

<style scoped>
.card {
    background-color: #121227;
    padding: 3rem 1rem 2rem;
    border-radius: 0.25rem;
}

.card__container-image {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #e1e1ff;
    border-radius: 50%;
    width: 120px;
    height: 120px;
    margin: 0 auto;
}

.card__image {
    display: block;
    width: 60%;
}

.card__title {
    color: #ffffff;
    font-weight: 300;
    text-align: center;
}

.card__button {
    display: block;
    font-family: 'Poppins', sans-serif;
    background-color: #21bbac;
    padding: 0.5rem 1rem;
    min-width: 120px;
    font-weight: 500;
    margin: 0 auto;
    cursor: pointer;
    text-transform: uppercase;
}

.card__button:hover {
    background-color: #0b9c8e;
    transition: background-color 0.3s ease;
}
</style>