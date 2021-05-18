<template>
  <div class="page-container">
            <!-- HEADER DESKTOP-->
           <HeaderContent/>
            <!-- END HEADER DESKTOP-->
            <!-- MAIN CONTENT-->
            <div class="main-content">
                <div class="section__content section__content--p30">
                    <div class="container-fluid">
                        <div class="row">
                            <div class="col-md-12">
                                <!-- DATA TABLE -->
                                <h3 class="title-5 m-b-35">data table</h3>
                                <TopTable/>
                                <div class="table-responsive table-responsive-data2">
                                    <table class="table table-data2">
                                        <thead>
                                            <tr>
                                                <th>Stt</th>
                                                <th>name</th>
                                                <th>email</th>
                                                <th>description</th>
                                                <th>date</th>
                                                <th>status</th>
                                                <th>price</th>
                                                <th>Edit</th>
                                                 <th>Delete</th>
                                                 {{sendItemProps.name}}
                                            </tr>
                                        </thead>
                                        <tbody>
                                       <Item v-for="item in items" v-bind:key="item.id" v-bind:itemsProps="item" />   
                                          
                                           
                                        </tbody>
                                    </table>
                                </div>
                                <!-- END DATA TABLE -->
                            </div>
                        </div>
                    
                    </div>
                </div>
            </div>
        </div>
</template>

<script>
import HeaderContent from './HeaderContent'
import TopTable from './TopTable'
import Item from './Item'
import {ref} from 'vue'

export default {
name:"Content",
components:{
HeaderContent,Item,TopTable

},
props:['sendItemProps'],

setup(){
    const items=ref([
      {
        id:1,
        name:"khuat van duc",
        email:"khuatduc12031999@gmail.com",
        dis:"like animals & riding cycle",
        date:"20/10/2020",
        process:"handed",
        price:3000
      },
      {
        id:2,
        name:"khuat van duc",
        email:"khuatduc12031999@gmail.com",
        dis:"like animals & riding cycle",
        date:"20/10/2020",
        process:"handed",
        price:3000
      },
      {
        id:3,
        name:"khuat van duc",
        email:"khuatduc12031999@gmail.com",
        dis:"like animals & riding cycle",
        date:"20/10/2020",
        process:"handed",
        price:3000
      },
    ])

   
     
      

    return{
      items,
     
    }
  }

}
</script>

<style>

</style>