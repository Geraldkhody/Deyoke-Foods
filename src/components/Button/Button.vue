<template>
    <a class="action" href="#" :style="customStyles">
        {{text}}
    </a>
</template>


<script>
import { ref } from 'vue'

export default {
    props: ["text", "color", "bg"],
    setup(props) {
        const customStyles = ref({
            backgroundColor: props.bg,
            color: props.color,
            borderColor: props.border
        })
        console.log(props)

        return {
            customStyles,
        }
    }
    
}
</script>

<script >  

</script>

<style scoped>
.action {
    border: 1px solid ;
    border-radius: 5px;
    padding: 0.5rem 1.1rem;
    font-weight: bold;
    font-size: 13px;
}

</style>