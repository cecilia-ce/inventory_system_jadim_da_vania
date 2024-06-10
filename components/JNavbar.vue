<template>
    <v-navigation-drawer 
        class="navbar"
        width="256" 
        disable-resize-watcher
    >
        <img 
            src="/public/assets/logo.png" 
            class="logo"
        />
        <div>
            <v-list-item class="pl-15 py-5" link title="PRODUTOS" href="../produtos"></v-list-item>
            <v-list-item class="pl-15 py-5" link title="FORNECEDORES"></v-list-item>
            <v-list-item class="pl-15 py-5" link title="VENDAS"></v-list-item>
        </div>
    </v-navigation-drawer>
</template>


<style scoped>

.navbar {
    background-color: #CCE6D3;
}

.logo {
    width: 100%;
}

/* .items {
    margin-left: 30px;
} */

</style>