<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{sale: theme === 'sale'}">
            <h1>{{header}}</h1>
            <p>{{text}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: ["theme"],
    methods: {
        closeModal(){
            this.$emit('close');
        }
    }
}


</script>

<style scoped>
.modal{
    width: 400px;
    padding: 20px;
    margin: 10px auto;
    background: white;
    border-radius: 10px;
}

.backdrop{
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}

h1{
    color:aqua;
    padding: 20px;
}

/* .modal.sale{
    background-color: cornflowerblue;
} */
</style>