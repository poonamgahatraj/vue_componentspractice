<template>

<h2>Popup Form</h2>
<p>Click on the button at the bottom of this page to open the login form.</p>
<p>Note that the button and the form is fixed - they will always be positioned to the bottom of the browser window.</p>

<button class="open-button" @click="displaypopup">Open Form</button>

<div class="form-popup" v-if="showpopup">
  <form style="    margin-left: 15px;
    margin-right: 15px;">
    <h1>Login</h1>

    <label for="email"><b>Email</b></label><br><br>
    <input type="text" placeholder="Enter Email"  style="    padding: 10px;
    width: 90%; background:#F1F1F1;border:none;"><br><br>

    <label for="psw"><b>Password</b></label><br><br>
    <input type="password" placeholder="Enter Password"   style="    padding: 10px;
    width: 90%; background:#F1F1F1;border:none;"><br><br>

    <button type="submit" class="btn"  >Login</button><br><br>
    <button type="button" class="btncancel" @click="removepopup">Close</button><br><br>
  </form>
</div>
</template>

<script>
export default{
    data(){
        return{
            showpopup:false
        }
    },

    methods:{
        displaypopup()
    {
        this.showpopup=true
    },

    removepopup(){
        this.showpopup=false
    }
    }
   

}
</script>

<style>
.open-button{
    background-color: #555;
  color: white;
  padding: 16px 20px;
  border: none;
  cursor: pointer;
  opacity: 0.8;
  position: fixed;
  bottom: 23px;
  right: 28px;
  width: 280px;
  z-index:1
}

.form-popup{
  
  
 position: fixed;
  bottom: 0;
  right: 2px;
  border: 3px solid #f1f1f1 ;
  z-index:3;

  border: 3px solid#F1F1F1;
    width: 25%;
}

.btn{
    padding: 18px;
    width: 98%;
    background:#36BB8A;
    border:none;
    color:white;
}


.btncancel{
    padding: 18px;
    width: 98%;
    background:#FF3333;
    border:none;
    color:white;
}

</style>