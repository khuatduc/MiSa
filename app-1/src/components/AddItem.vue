<template>
  <div class="container">
      <div class="row">
          <form class="form1" @submit="sendItem">
              <h3>Add a new Item</h3>
          <div class="form-group row">
              <label class="col-sm-1-12 col-form-label">Enter Name</label>
              <div class="col-sm-1-12">
                  <input type="text" class="form-control" name="name" v-model="item.name"   placeholder="">
              </div>
          </div>
          <div class="form-group row">
              <label class="col-sm-1-12 col-form-label">Enter Email</label>
              <div class="col-sm-1-12">
                  <input type="text" class="form-control" name="Email" v-model="item.email"  placeholder="">
              </div>
          </div>
          <div class="form-group row">
              <label class="col-sm-1-12 col-form-label">Discription</label>
              <div class="col-sm-1-12">
                  <input type="text" class="form-control" name="Discript" v-model="item.dis" placeholder="">
              </div>
          </div>
          <div class="form-group row">
              <label class="col-sm-1-12 col-form-label">Enter DatePublish</label>
              <div class="col-sm-1-12">
                  <input type="date" class="form-control" name="Date" v-model="item.date"  placeholder="">
              </div>
          </div>
            <div class="form-group row">
              <label class="col-sm-1-12 col-form-label">Enter Status</label>
              <div class="col-sm-1-12">
                  <input type="text" class="form-control" name="Staus" v-model="item.status" placeholder="">
              </div>
          </div>
           <div class="form-group row">
              <label class="col-sm-1-12 col-form-label">Enter Price</label>
              <div class="col-sm-1-12">
                  <input type="text" class="form-control" name="Price" v-model="item.price"  placeholder="">
              </div>
          </div>
          <div class="form-group row">
              <div class="offset-sm-2 col-sm-10">
                  <button type="submit" class="btn btn-primary" >Comfirm</button>
                  <button type="" class="btn btn-success" id="close">Close</button>
              </div>
          </div>
         
      </form>
      </div>
  </div>
</template>

<script>
import {ref} from 'vue'
export default {
 name:"AddItem",
 setup(props, context){
     const item=ref({
         id:"",
         name:"",
         email:"",
         dis:"",
         date:"",
         status:"",
         price:""
     })

     const sendItem=event=>{
        event.preventDefault()
        const newItem={
         id:4,
         name:item.value.name,
         email:item.value.email,
         dis:item.value.dis,
         date:item.value.date,
         status:item.value.status,
         price:item.value.price
        }

         context.emit('oneItem',newItem)
        item.value.name="",
        item.value.email="",
        item.value.dis="",
        item.value.date="",
        item.value.status="",
        item.value.price=""
     }

    
     
     return {
         item,
         sendItem
         
     }
 }
}
</script>

<style scoped>

.form1 {
    background: #7fb169e0;
    position: absolute;
    width: 25%;
    border: 1px solid #bdbd4273;
    top: 18%;
    left: 36%;
    z-index: 6;
    padding-left: 60px;
}

.form1 input {
    width: 90%;
}

.row{
    display: block;
}

h3 {
    text-align: center;
    margin: 0px;
    padding-top: 30px;
    
}

button.btn.btn-primary {
  margin-right: 30px`;
}
</style>