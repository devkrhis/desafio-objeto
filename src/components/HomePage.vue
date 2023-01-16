<template>
    <div id="arrayObject">
        <ListPerson :items="items"/>
        <button type="button" @click="setItems"> Add New Item</button>
    </div>
    
</template>

<script>
/* eslint-disable */ 
import ListPerson from './ListPerson.vue';

export default {
    components: {
        ListPerson
    },
    data(){
        return {
            items: [
            {
                ID: 0,
                Nome: "Krhis",
                Idade: 0,
                Local: {
                    Cidade: "Curitiba",
                    Estado: "Paraná"
                }
            },
            {
                ID: 1,
                Nome: "Krhiws",
                Idade: 1,
                Local: {
                    Cidade: "Curitiba",
                    Estado: "Paraná"
                }
            }
            ]
        }
    },
    methods: {
        setItems(){
            const newItem = 
            {
                ID: 2,
                Nome: "Rafa Lindu",
                Idade: 2,
                Local: {
                    Cidade: "Curitiba",
                    Estado: "Paraná"
                }
            }

            this.items.push(newItem)
        }
    }
    
}
</script>

<style scoped>

</style>