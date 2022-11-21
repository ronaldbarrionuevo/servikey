<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { Link } from '@inertiajs/inertia-vue3';
import ActionSection from '../../Components/ActionSection.vue';

defineProps({
    clientes: Object,
});
</script>
<template>
    <AppLayout>
        <template #header> titulo</template>
        <template #default>
            <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                <ActionSection>
                    <template #title>cliente</template>
                    <template #description>Mostrar los clientes </template>
                    <template #content>
                        <p>{{clientes.descripcion_cliente}}</p>
                        <p>{{clientes.telefono}}</p>
                        <Link :href="route('Cliente.index')" as="button" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full ">volver</Link>
                    </template>
                </ActionSection>
            </div>
        </template>
    </AppLayout>
</template>