<template>
    <div id="listAssembler">
            <tr>
                <td> ID </td>
                <td> Nome </td>
                <td> Idade </td>
                <td> Cidade </td>
                <td> Estado </td>
            </tr>
            <div v-for="value in items" :key="value.id">
                <tr>
                    <td> {{ value.ID }} </td>
                    <td> {{ value.Nome }}</td>
                    <td> {{ value.Idade }}</td>
                    <td> {{ value.Local.Cidade }}</td>
                    <td> {{ value.Local.Estado }}</td>
    
                </tr>
            </div>
    </div>
    
</template>

<script>
export default {
    /* eslint-disable */
    props: {
        items: {
            type: Object
        }
    }
    
}
</script>

<style scoped>

#listAssembler td, tr{
    border: 1px solid black;
    background: #acacac31;
    padding: 10px;
    
}



</style>