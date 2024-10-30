<template>
    <Container class="about-us">
        <h1>{{ props.title }}</h1>
        <p>{{ props.body }} </p>
    </Container>
</template>

<script setup>
import Container from "@/components/Container/Container.vue"
import { defineProps } from "vue"

const props = defineProps({
    title: {
        type: String,
        required: true
    },
    body: {
        type: String,
        required: true
    }
})

// console.log(props)

</script>

<style scoped>
.about-us {
    text-align: center;
    padding: 20px;
    color: #333;
}

h1 {
    color: var(--primary-color);
    margin-bottom: 10px;
}
</style>