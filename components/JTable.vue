<template>
    <v-data-table
        :headers="headers"
        :items="products"
        class="table custon-table"
    >
        <template v-slot:item.actions="{ item }">
            <v-icon class="me-2" size="small" @click="editItem(item)">
                mdi-pencil
            </v-icon>
            <v-icon size="small" @click="deleteItem(item)"> mdi-delete </v-icon>
        </template>
    </v-data-table>
</template>

<script setup>
const headers = [
    {
        title: 'Produto', 
        key: 'product',
    },
    { 
        title: 'Fornecedor', 
        key: 'provider' 
    },
    { 
        title: 'Quantidade', 
        key: 'amount' 
    },
    { 
        title: 'Valor de venda', 
        key: 'saleValue' 
    },
    { 
        title: 'Actions', 
        key: 'actions', 
        sortable: false 
    },
]

const products = ref([
    {
        id: 1,
        product: "Cacto",
        provider: "João Oliveira ME",
        amount: 5,
        saleValue: "R$ 7,00"
    },
    {
        id: 2,
        product: "Suculenta pequena",
        provider: "Plantas Bonitas Loja",
        amount: 2,
        saleValue: "R$ 10,00"
    },
    {
        id: 3,
        product: "Cacto Médio",
        provider: "João Oliveira ME",
        amount: 3,
        saleValue: "R$ 10,00"
    },
    {
        id: 4,
        product: "Cacto",
        provider: "João Oliveira ME",
        amount: 5,
        saleValue: "R$ 7,00"
    },
    {
        id: 5,
        product: "Samanbaia",
        provider: "Loja de Plantas",
        amount: 5,
        saleValue: "R$ 50,00"
    },
    {
        id: 6,
        product: "Rosa do Deserto",
        provider: "Loja de Plantas",
        amount: 10,
        saleValue: "R$ 80,00"
    },
    {
        id: 7,
        product: "Cacto",
        provider: "João Oliveira ME",
        amount: 5,
        saleValue: "R$ 7,00"
    },
    {
        id: 8,
        product: "Cacto",
        provider: "João Oliveira ME",
        amount: 5,
        saleValue: "R$ 7,00"
    },
])
</script>

<style scoped>
.table {
    width: 50vw;
    border-radius: 20px;
    color: #254E43;
    font-size: 16px;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2); 
    padding: 3%;
}
</style>