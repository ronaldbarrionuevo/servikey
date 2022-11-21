<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import ActionSection from '../../Components/ActionSection.vue'
defineProps({
    clientes: Array,
});
</script>

<template>
    <AppLayout>
        <template #header>
            Cliente
        </template>
        <!-- <p v-for="juan in clientes">{{juan}}</p> -->
        <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
        <ActionSection>
            <template #title>lista de cliente</template>
            <template #description>Mostrar los clientes activos</template>
            <template #content>
                <table class="w-full">
                    <thead>
                        <tr>
                            <th>Descripcion Cliente</th>
                            <th>Telefono</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="clientes in clientes">
                            <td>{{ clientes.descripcion_cliente }}</td>
                            <td>{{ clientes.telefono }}</td>
                        </tr>
                    </tbody>
                </table>
            </template>
        </ActionSection>
    </div>
    </AppLayout>


</template>