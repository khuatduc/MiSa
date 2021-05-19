<template>
    <div class="page-wrapper">
      <div class="baoboc"></div>
        <Header/>
        <!-- MENU SIDEBAR-->
       <Sidebar/>
        <!-- END MENU SIDEBAR-->
        <Content v-bind:sendItemProps="addItem" />
        <AddItem @oneItem="addItem"/>
        <!-- PAGE CONTAINER-->
        <Footer/>

    </div>

   
  
</template>

<script>
import Header from './components/Header'
import Sidebar from './components/Sidebar'
import Content from './components/Content'
import Footer from './components/Footer'
import AddItem from './components/AddItem'
import {ref} from 'vue'

export default {
  name: 'App',
  components: {
    Header,Sidebar,Content,Footer,AddItem
  },

  setup(){
    const item=ref({
         id:"",
         name:"",
         email:"",
         dis:"",
         date:"",
         status:"",
         price:""
     })

    const addItem=newTodo=>{
        item.value.id=newTodo.id,
        item.value.name=newTodo.name,
        item.value.email=newTodo.email,
        item.value.dis=newTodo.dis,
        item.value.date=newTodo.date,
        item.value.status=newTodo.status,
        item.value.price=newTodo.price
    }
    
    return{
      addItem
    }
   
  }
  
}

</script>

<style>
.baoboc {
    position: absolute;
    background: black;
    width: 100%;
    height: 100%;
    top: 0px;
    left: 0;
    z-index: 4;
    opacity: 0.5;
}
</style>
