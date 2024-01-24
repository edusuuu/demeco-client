<script>
    import { createEventDispatcher } from 'svelte';
const fuel = [
    {
        type:"Diesel",
        price:"59"
    },
    {
        type:"Regular",
        price:"55"
    },
    {
        type:"Unleaded",
        price:"57"
    }
]


const dispatch = createEventDispatcher();

let fuelTypeToEdit = '';
let newPrice = '';

function editPrice() {
  const index = fuel.findIndex(fuelItem => fuelItem.type === fuelTypeToEdit);

  if (index !== -1) {
    fuel[index].price = newPrice;
    dispatch('editPrice', fuel);
  }
}
</script>

<table class="userlist">
    <tr class="titles">
      <td>Fuel type</td>
      <td>Price</td>
    </tr>
    {#each fuel as fuelItem}
      <tr>
        <td class="td">{fuelItem.type}</td>
        <td class="td">{fuelItem.price}</td>
      </tr>
    {/each}
  </table>
  
  <div class="adminEdit">
    <div>
      <input class="txtBox" bind:value={fuelTypeToEdit} placeholder="Enter Target Fuel Type" />
      <input class="txtBox" bind:value={newPrice} placeholder="Enter New Price" />
      <button class="btnSide2" on:click={editPrice}>Confirm</button>
    </div>
  </div>

<style>
    .userlist {
  border: 2px;
  border-style: solid;
  height: 300px;
  overflow-y: scroll;
  overflow-x: scroll;
  width: 800px;
  display: block;
}

td {
width:fit-content;
border: 1px;
border-style: solid;
height: 40px;
}

.txtBox{
    font-size: 13px;
    padding: 10px 20px;
    width: 100%;
    outline: none;
    background: #d3b5f0;
    color: #000000;
    border: 1px solid #62457c;
    border-radius: 100px;
    transition: 0.3s ease;
    margin: 5px;
    width: 450px;
    opacity: 0.65;
}

table {
  margin: 50px;
  block-size: 100px;
  margin-left: 120px;
  border-collapse: separate;
  border: solid rgb(245, 245, 245) 1px;
  border-radius: 6px;
  color: white;
}
.titles{
    background:#371d50;
    font-weight: bold;
}
.td{
    width: fit-content;
    min-width: 150px;
   align-items: center;
   padding-left: 5px;
    
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


</style>