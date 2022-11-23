<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import FormSection from '../../Components/FormSection.vue';
import InputLabel from '../../Components/InputLabel.vue';
import TextInput from '../../Components/TextInput.vue'
function enviar(){

}
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
                            <TextInput type="text" name="descripcion_cliente" id="descripcion_cliente"></TextInput>
                        </div>
                        <div class="col-span-6 sm:col-span-4">
                            <InputLabel for="telefono" value="Telefono" />
                            <TextInput type="text" name="telefono" id="telefono"></TextInput>
                        </div>
                        
                    </template>
                    <template #actions>botonwees</template>
                </FormSection>
            </div>
        </template>
    </AppLayout>
</template>