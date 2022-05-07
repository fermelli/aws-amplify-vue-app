<script>
import CardFeature from './components/CardFeature.vue'
export default {
    name: 'App',
    components: {
        CardFeature
    },
    data() {
        return {
            features: [
                {
                    title: 'Goal',
                    count: 0,
                    image: {
                        src: 'goal.png',
                        alt: 'Goal'
                    }
                },
                {
                    title: 'Idea',
                    count: 0,
                    image: {
                        src: 'idea.png',
                        alt: 'Idea'
                    }
                },
                {
                    title: 'Performance',
                    count: 0,
                    image: {
                        src: 'performance.png',
                        alt: 'Performance'
                    }
                },
                {
                    title: 'Target',
                    count: 0,
                    image: {
                        src: 'target.png',
                        alt: 'Target'
                    }
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <h1 class="title">Features</h1>
        <div class="container-cards">

            <CardFeature v-for="feature in features" :feature="feature" @add-to-count="feature.count++" />

        </div>
    </div>
</template>

<style>
.container {
    max-width: 1200px;
    margin: 0 auto;
}

.title {
    color: #ffffff;
}

.container-cards {
    display: grid;
    gap: 2rem;
    grid-template-columns: repeat(4, minmax(200px, 25%));
}
</style>
