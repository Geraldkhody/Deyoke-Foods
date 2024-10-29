<template>
    <Container>
        <h1>
            <span class="welcome">Welcome <span style="color: #9FE82B">to</span></span><br>
            <span class="large">Deyoke Foods</span>
        </h1>
        <p>Join the organic movement today</p>
        <img src="@/assets/tur berry.png" alt="">
    </Container>
</template>

<script setup>
import Container from "@/components/Container/Container.vue"


</script>

<style scoped>
.container {
    margin-bottom: auto;
    color: white;
    margin-top: -60px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100%;
}

h1 {
    font-size: 2.5rem;
}

.large {
    font-size: 4rem;
}

p {
    margin-top: 5px;
}

img {
    width: 150px;
    margin-top: 10px;
}


@media (max-width: 1023px) {
    h1 {
        font-size: 2rem;
    }

    .large {
        font-size: 3rem;
        letter-spacing: 2px;
    }

    img {
        width: 120px;
    }
}

@media (max-width: 767px) {
    h1 {
        font-size: 1.5rem;
    }

    .large {
        font-size: 2.5rem;
    }

    img {
        font-size: 1rem;
    }
}

</style>