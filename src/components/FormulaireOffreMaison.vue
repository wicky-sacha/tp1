<script setup lang="ts">
    import { ref } from "@vue/reactivity";
    import Card from "./card.vue";

    const maison = ref ({});
</script>
<template>
    <div>
        <div class="p-2">
            <h2 class="text-2xl">Résultat (Prévisualisation)</h2>
            <Card v-bind="maison" />
        </div>
        <div class="p-2">
            <FormKit type="form" v-model="maison"
            :config="{
                classes: {
                    input: 'p-1 rounded border-gray-300 shadow-sm border',
                    label: 'text-gray-600',},
                    }"
            :submit-attrs="{ classes: { input: 'bg-red-300 p-1 rounded' }
            }">
                <FormKit name="nom" label="Nom" />
                <FormKit name="price" label="Prix" type="name" />
                <FormKit name="favori" label="Mettre en valeur" type="checkbox" wrapper-class="flex" />
                <FormKit name="bain" label="Nombre de salle de bain" type="number" />
                <FormKit name="surface" label="Surface m2" type="number" />
            </FormKit> 
        </div>
    </div>
</template>


