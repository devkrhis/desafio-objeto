<template>
    <div id="arrayObject">
        <ListPerson :items="items" 
        @testeRemove="alterarLista"
        />
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
            randomNumber: 1,
            contador: 0,
            items: [
            {
                id: 0,
                Nome: "Krhis",
                Idade: 0,
                Local: {
                    Cidade: "Curitiba",
                    Estado: "Paraná"
                }
            },
            {
                id: 1,
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
            this.randomNumber++
            const newItem = 
            {
                id: this.randomNumber,
                Nome: "Rafa Lindu" + this.randomNumber,
                Idade: 2,
                Local: {
                    Cidade: "Curitiba",
                    Estado: "Paraná"
                }
            }

            this.items.push(newItem)
        },
        alterarLista(newEvent){
            console.log(newEvent)
            // this.items.splice(newEvent, 1)

            let numbersIndex = this.items
            let elementIndex = numbersIndex.findIndex(el => el.id == newEvent)
            console.log("elemento", elementIndex)
            this.items.splice(elementIndex, 1)
            

        }
    }
    
}
</script>

<style scoped>

</style>