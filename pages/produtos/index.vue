<template>
    <div>
        <j-header></j-header>
        <j-navbar></j-navbar>
        
        <main class="product-main d-flex flex-column justify-center align-center mt-16 ga-10">
            <div class="d-flex flex-column align-end ga-10">
                <v-btn
                    variant="outlined"
                    color="#254E43"
                    size="large"
                    class="button rounded-lg"
                >
                    Cadastrar Produto
                </v-btn>
                <j-table />
            </div>
        </main>
    </div>
</template>

<script setup>



</script>

<style>
.button {
    font-weight: 700 !important;
}
</style>