<template>
    <tr class="tr-shadow">
                                                <td>{{itemsProps.id}}</td>
                                                <td>{{itemsProps.name}}</td>
                                                <td>
                                                    <span class="block-email">{{itemsProps.email}}</span>
                                                </td>
                                                <td class="desc">{{itemsProps.dis}}</td>
                                                <td>{{itemsProps.date}}</td>
                                                <td>
                                                    <span class="status--process">{{itemsProps.process}}</span>
                                                </td>
                                                <td>{{itemsProps.price}}</td>
                                                <td>Edit </td>
                                                 <td>Delete </td>
    </tr>
</template>

<script>
export default {
name:'Item',
props:['itemsProps']
}
</script>

<style>

</style>