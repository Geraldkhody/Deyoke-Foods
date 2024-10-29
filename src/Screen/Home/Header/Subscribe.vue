<template>
    <div class="wrapper">
        <Container>
        <div class="content">
            <h2>Subscribe for more product updates</h2>
            <p>We work towards providing affordable products and quality services to our customers. Get product updates through newsletter</p>
        </div>
        <div class="input-field">
            <input type="text" class="input" placeholder="Enter your email address"  />
            <button>Subscribe</button>
        </div>
        </Container>
    </div>
</template>

<script setup>
import Container from "@/components/Container/Container.vue"

</script>

<style scoped>
.wrapper {
    background: #014751;
}

.container {
    display: flex;
    align-items: center;
    gap: 5rem;
    padding: 2rem 0;

}

.content{
    width: 40%;
}

h2 {
    color: #9FE82B;
}

p {
    color: #fff;
    font-size: 13px;
    letter-spacing: 1.3px;
    line-height: 1.5;
    word-spacing: 2px;
}

.input-field {
    min-width: 50%;
    display: flex;
    gap: 1rem;
}

input {
    padding: 1rem 1rem;
    border-radius: 10px;
    width: 100%;
    font-size: 14px;
}

button {
    background: transparent;
    color: white;
    border: 1px solid ;
    border-radius: 5px;
    padding: 0.8rem 2rem;
    font-weight: bold;
    cursor: pointer;
}

button:hover {
    background-color: #eee;
    color: var(--primary);
}


@media (max-width: 1023px) {
    .container {
        padding: 1rem 0;
        flex-direction: column;
        gap: 1rem;
    }

    .content {
        width: 100%;
    }

    .input-field {
        width: 100%;
    }

    .content h2 {
        font-size: 1.3rem;
    }

    .content p {
        font-size: 12px;
        /* letter-spacing: 1px;
        word-spacing: 1px; */
    }

    input {
        padding: 0 0.8rem;
        font-size: 13px;
    }

    button {
        padding: 0.7rem 1.5rem;
        font-size: 13px;
    }
}

</style>