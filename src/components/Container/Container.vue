<template>
    <div class="container">
        <slot />
    </div>
</template>

<style scoped>
.container {
    width: 80%;
    margin: auto;
}


@media (max-width: 1024px) {
    .container {
        width: 85%;
    }
}


@media (max-width: 767px) {
    .container {
        width: 90%;
    }
}

</style>