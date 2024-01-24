<script>
    import { goto } from '$app/navigation'
    import AcceptedOrder from '../../components/AcceptedOrder.svelte';


    let orderVisible = false;
    function toggleVisibility() {
    orderVisible = !isVisible;
  }

  function handleEditStatus(event) {
  
    console.log('Edit status event received:', event.detail);
  }
    
</script>
<div class="admin">
    <h1><b>Welcome Delivery Man!</b></h1>
    <div class="adminPage">
      <input type="button" value="Pending Orders" class="btnSide2" on:click={toggleVisibility} />
    </div>

    {#if orderVisible}
    <AcceptedOrder on:editStatus={handleEditStatus} />
    {/if}
 

  
  </div>
<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.admin {
  min-height: 100vh;
  font-family: Arial, Helvetica, sans-serif;
  padding: 15px;
}

.admin > h1 {
  margin-top: 20px;
  color: #ffffff;
}



.adminPage {
  margin: 20px;
  font-family: Arial, Helvetica, sans-serif;
}



.btnSide1 {
  background-color: #ffffff;
  border-radius: 28px;
  border: 1px solid #ffffff;
  display: inline-block;
  color: #35104b;
  cursor: pointer;
  font-weight: bold;
  margin-left: 50px;
  width: 150px;
  font-size: larger;
  min-height: 40px;
  text-shadow: 0px 1px 0px #2a2d2a;
}
.btnSide1:hover {
  background-color: #c26df7;
  color: white;
}

.btnSide1:active {
  position: relative;
  color: white;
  top: 2px;
}

.btnSide2 {
  background-color: #ffffff;
  border-radius: 28px;
  border: 1px solid #ffffff;
  display: inline-block;
  cursor: pointer;
  color: #35104b;
  font-weight: bold;
  margin-left: 50px;
  width: 180px;
  font-size: larger;
  min-height: 40px;
  text-shadow: 0px 1px 0px #2a2d2a;
}
.btnSide2:hover {
  background-color: #a964f8;
  color: white;
}

.btnSide2:active {
  position: relative;
  color: white;
  top: 2px;
}

.adminEdit {
  margin: 20px;
  font-family: Arial, Helvetica, sans-serif;
}



.fields{
  visibility: hidden;
}


</style>