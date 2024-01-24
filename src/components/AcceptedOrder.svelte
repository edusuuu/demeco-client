<script>
    import { createEventDispatcher } from 'svelte';
     const Orders = [
    {
    orderID:"0001",
    name:"Edzel John Angeles",
    email:"user@gmail.com",
    phonenum:"09123456789",
    status:"Pending"
    },
    
    {
    orderID:"0002",
    name:"Edzel John Angeles",
    email:"user@gmail.com",
    phonenum:"09123456789",
    status:"Approved"
    },
    
    {
    orderID:"0003",
    name:"John Edrian Ordonio",
    email:"jed123@gmail.com",
    phonenum:"09465321987",
    status:"Pending"
    },
    {
    orderID:"0004",
    name:"Marian Kariel Ordonie",
    email:"mariankarielordonio@yahoo.com",
    phonenum:"09789456123",
    status:"Pending"
    },
    
    {
    orderID:"0005",
    name:"Edzel John Angeles",
    email:"user@gmail.com",
    phonenum:"09123456789",
    status:"Approved"
    },

    {
    orderID:"0006",
    name:"Mark Angelo Torres",
    email:"Rakbu@gmail.com",
    phonenum:"09717113116",
    status:"Approved"
    }
    
    ]
    
    const dispatch = createEventDispatcher();
    
    let orderIDToUpdate = '';
    
    function editStatus() {  const index = Orders.findIndex(order => order.orderID === orderIDToUpdate);
    
    
      if (index !== -1) {
        Orders[index].status = 'Accepted';
    
        dispatch('editStatus', Orders);
      }
    }
    </script>
    
    <table class="userlist">
          <tr class="titles">
            <td>OrderID</td>
            <td>Name</td>
            <td>Email</td>
            <td>Phonenum</td>
            <td>Status</td>
          </tr>
        {#each Orders.filter(order => order.status == 'Approved') as order } 
          <tr>
            <td class="td">{order.orderID}</td>
            <td class="td">{order.name}</td>
            <td class="td">{order.email}</td>
            <td class="td">{order.phonenum}</td>
            <td class="td">{order.status}</td>
            
        </tr>
        
        {/each}
    </table>
    <div class="adminEdit">
    <input class="txtBox" bind:value={orderIDToUpdate} placeholder="Enter OrderID" />
    <button class="btnSide2" on:click={editStatus}>Approve</button>
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
        