<template>
  <div id="overlay" style="display: none;">
   <div class="modal-dialog">
     <div class="modal-content">
       <div class="modal-header">
          <h5 class="modal-title">{{ modalTitle }}</h5>
          <button type="button" class="close" onclick="hideElement('overlay')">
            <span aria-hidden="true">&times;</span>
          </button>
       </div>
       <div class="modal-body p-4">
         <form action="#" @submit="postData">
           <div class="form-group">
             <input type="text" name="name" class="form-control form-control-lg mb-3" placeholder="Name" v-model="customer.name">
             <input type="text" name="address" class="form-control form-control-lg mb-3" placeholder="Address" v-model="customer.address">
             <input type="text" name="phone" class="form-control form-control-lg mb-3" placeholder="Phone" v-model="customer.phone">
             <input type="email" name="email" class="form-control form-control-lg mb-3" placeholder="Email" v-model="customer.email">
             <input type="number" name="age" class="form-control form-control-lg mb-3" placeholder="Age" v-model="customer.age">
             <div class="d-flex justify-content-center">
                <button class="btn btn-info btn-lg" onclick="hideElement('overlay')">{{ modalTitle }}</button>
             </div>
           </div>
         </form>
       </div>
     </div>
   </div>
 </div>
</template>

<script>
import axios from 'axios'

export default {
  name: "OrganismAddModal",
 props: {
    modalTitle: String
  },
  data(){
    return{
      customer:{
        name: null,
        address: null,
        phone: null,
        email: null,
        age: null
      }
    }
  },
  methods:{
    postData(e){
      if(this.customer.name != null && this.name.trim().length > 0 &&
      this.customer.address != null && this.name.trim().length > 0 &&
      this.customer.phone != null && this.phone.trim().length > 0 &&
      this.customer.email != null && this.email.trim().length > 0 &&
        this.customer.age != null && this.customer.age > 0)
      {
        axios.post("http://localhost:7071/api/Saver", this.customer)
        .then((result)=>{
            console.log(result);
            document.getElementById("successMsg").style.display = "block"
        })
        .catch(error => {
            console.log(error);
             document.getElementById("errorMsg").style.display = "block"
        });
      }
      else
      {
        document.getElementById("errorMsg").style.display = "block"
        document.getElementById("innerError").innerHTML = "All fields are mandatory"
      }

      e.preventDefault();
    },
  }
};
</script>