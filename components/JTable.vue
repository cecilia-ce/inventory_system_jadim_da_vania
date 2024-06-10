<template>
    <v-data-table
        :headers="headers"
        :items="products"
        class="table custon-table"
    >
        <template v-slot:item.actions="{ item }">
            <v-icon class="me-2" size="small" @click="editProduct(item)">
                mdi-pencil
            </v-icon>
            <v-icon size="small" @click="deleteItem(item)"> mdi-delete </v-icon>
        </template>
    </v-data-table>
    
    <v-dialog
      v-model="isEditModalOpen"
      width="auto"
    >
    <v-card
        width="40vw"
        class="pa-10 card rounded-xl"
    >
        <h1 class="mb-10">Editar produto</h1>
        <div class="d-flex ga-5">
            <v-text-field
                variant="outlined"
                label="Nome*"
                class="inputs"
            />
            <v-text-field
                variant="outlined"
                label="Fornecedor"
                class="inputs"
            />
        </div>
        <div class="d-flex ga-5">
            <v-text-field
                variant="outlined"
                label="Quantidade*"
                class="inputs"
            />
            <v-text-field
                variant="outlined"
                label="Custo unitário*"
                class="inputs"
            />
            <v-text-field
                variant="outlined"
                label="Preço de venda (Unitário)*"
                class="inputs"
            />
        </div>
        <v-textarea 
            variant="outlined"
            label="Descrição"
            placeholder="Descrição"
            class="inputs"
        />
        
        <v-card-actions class="d-flex justify-center">
            <v-btn
              color="#254E43"
              variant="outlined"
              @click="close"
            >
              Cancelar
            </v-btn>
            <v-btn
              color="#254E43"
              variant="outlined"
              @click="save"
            >
              Salvar
            </v-btn>
        </v-card-actions>
    </v-card>
    </v-dialog>
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

const isEditModalOpen = ref(false)

function editProduct(item) {
    isEditModalOpen.value = true
}
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

.inputs {
    color: #254E43;
    border-radius: 25px;
}

.card {
    text-align: center;
    color: #254E43;
}
</style>