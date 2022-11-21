<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import ActionSection from '@/Components/ActionSection.vue';
import { Link } from '@inertiajs/inertia-vue3';



defineProps({
    clientes: Array,
});
</script>

<template>
    <AppLayout>
        <template #header>
            <Link v-bind:href="route('Cliente.create')" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Crear Cliente</Link>
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
                                <th>ver</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for="clientes in clientes">
                                <td>{{ clientes.descripcion_cliente }}</td>
                                <td>{{ clientes.telefono }}</td>
                                <td>
                                    <!-- <Link v-bind:href="route('Cliente.show')" -->
                                        <!-- class="text-sm text-gray-700 dark:text-gray-500 underline">ver</Link> -->
                                    <Link :href="route('Cliente.show',clientes.id)" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full " as="button">ver</Link>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </template>
            </ActionSection>
        </div>
    </AppLayout>


</template>