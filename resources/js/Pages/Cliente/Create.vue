<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import FormSection from '@/Components/FormSection.vue';
import InputLabel from '@/Components/InputLabel.vue';
import TextInput from '@/Components/TextInput.vue';
import InputError from '@/Components/InputError.vue';
import { useForm } from '@inertiajs/inertia-vue3';

const form = useForm({
    descripcion_cliente:'',
    telefono : '',
});
function enviar(){
    console.log('FORMUALARIO ');
};
</script>
<template>
    <AppLayout>
        <template #header>Formulario de crear Cliente</template>
        <template #default>
            <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                <FormSection @submitted="enviar()">
                    <template #title>Titulo</template>
                    <template #description>Ddesciocion</template>
                    <template #form>
                        <div class="col-span-6 sm:col-span-4" >
                            <InputLabel for="descripcion_cliente" value="Descripcion Cliente" />
                            <TextInput type="text" name="descripcion_cliente" id="descripcion_cliente" v-model="form.descripcion_cliente" class="w-full"></TextInput>
                            <InputError v-bind:message="form.errors.descripcion_cliente"></InputError>
                        </div>
                        <div class="col-span-6 sm:col-span-4">
                            <InputLabel for="telefono" value="Telefono" />
                            <TextInput type="text" name="telefono" id="telefono" v-model="form.telefono" class="w-full"></TextInput>
                            <InputError v-bind:message="form.errors.telefono"></InputError>
                        </div>
                        
                    </template>
                    <template #actions>
                        <button type="submit"> gusardare</button>
                    </template>
                </FormSection>
            </div>
        </template>
    </AppLayout>
</template>