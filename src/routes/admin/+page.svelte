<script>
    import { goto } from '$app/navigation'
    import Users from '../../components/Users.svelte';
    import Orderinfo from '../../components/Orderinfo.svelte';
    import FuelPrice from '../../components/FuelPrice.svelte';

    let isVisible = false;
    let orderVisible = false;
    let fuelVisible = false;
    function toggleVisibility() {
    isVisible = !isVisible;
    
  }
  
    function toggleVisibilityOrder() {
    orderVisible = !orderVisible;
  }

  function toggleVisibilityfuel() {
    fuelVisible = !fuelVisible;
    
  }

  function handleEditStatus(event) {
  
    console.log('Edit status event received:', event.detail);
  }
  function handleEditPrice(event) {
    // Update the local fuelData with the edited data from the FuelComponent
    fuelData = event.detail;
  }
</script>
<div class="admin">
    <h1><b>Welcome Admin!</b></h1>
    <div class="adminPage">
      <input type="button" value="User List" class="btnSide1" on:click={toggleVisibility}/>
      <input type="button" value="Pending Orders" class="btnSide2" on:click={toggleVisibilityOrder} />
      <input type="button" value="Fuel Prices" class="btnSide2" on:click={toggleVisibilityfuel} />
    </div>

    {#if isVisible}
    <Users />
    {/if}
    {#if orderVisible}
    <Orderinfo on:editStatus={handleEditStatus} />
    {/if}

    {#if fuelVisible}
    <FuelPrice on:editPrice={handleEditPrice}/>
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