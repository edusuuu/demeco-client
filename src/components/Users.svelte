<script>
const Users = [
    {
    bday:"2004-12-14",
    email: "mariankarielordonio@yahoo.com",
    fname:"Marian Kariel",
    gender:"Female",
    lname:"Ordonie",
    password:"$2b$10$L6FRk7L7Fo.VTg4bXfkL8uAj74KAZcNjnYhyp.T3iVqlPKYGIm0Fa",
    phonenum:"09789456123",
    role:"Customer"
},
{
    bday:"2003-09-11",
    email: "jed123@gmail.com",
    fname:"John Edrian",
    gender:"Male",
    lname:"Ordonio",
    password:"2b$10$xN.y0.msV/GJoi3Wp9ZKYOqiZpDHlqA0xfdOicRoEyoNmYtJ2z7jO",
    phonenum:"09465321987",
    role:"Delivery man"
},

{
    bday:"2023-12-31",
    email: "meros12125344@gmail.com",
    fname:"testing",
    gender:"Male",
    lname:"or password",
    password:"$2b$10$bDK/X76o2BKoCmlEPkP.9u5W2cUOwI8ZNW.dPNIr.aDAsmwF1pLw2",
    phonenum:"09987654321",
    role:"Customer"
},
{
    bday:"2000-10-10",
    email: "test123@gmail.com",
    fname:"test man",
    gender:"Male",
    lname:"XD",
    password:"2b$10$CqzQC2Dj2.eHmyh4li0bPO5/TNOoHEV.ACKmemjwQMp7GntWhZc1C",
    phonenum:"09123456789",
    role:"Delivery man"
},
{
    bday:"2000-10-10",
    email: "edzeljohnangeles@gmail.com",
    fname:"Edzel John",
    gender:"Male",
    lname:"Angeles",
    password:"$2b$10$KCbW8Un.7Y4kLgiX1W6ThOnX2AvmTdkTadlaeK8IjA5Bu/XT7a6lm",
    phonenum:"09454612977",
    role:"Admin"
},
{
    bday:"2000-10-10",
    email: "user@gmail.com",
    fname:"Edzel John",
    gender:"Male",
    lname:"Angeles",
    password:"$2b$10$zOoYQTV95cDFUI2h58wUUOBhyhdZBMzE2e2928RuTRQ0iBiHyElym",
    phonenum:"09123456789",
    role:"Customer"
}

]

</script>

<table class="userlist">
      <tr class="titles">
        <td>Fname</td>
        <td>Lname</td>
        <td>Birthdate</td>
        <td>Gender</td>
        <td>Phone num</td>
        <td>E-mail</td>
        <td>Role</td>
        <td>Password</td>
      </tr>
      {#each Users as user}
      <tr>
        <td class="td">{user.fname}</td>
        <td class="td">{user.lname}</td>
        <td class="td">{user.bday}</td>
        <td class="td">{user.gender}</td>
        <td class="td">{user.phonenum}</td>
        <td class="td">{user.email}</td>
        <td class="td">{user.role}</td>
        <td class="td">{user.password}</td>
      </tr>
    
      
      {/each}
    </table>

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

</style>