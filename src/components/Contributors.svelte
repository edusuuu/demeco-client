<script>
  import edzel from "$lib/images/contributor/edzel.jpg";
  import meryliza from "$lib/images/contributor/meryliza.jpg";
  import dannel from "$lib/images/contributor/dannel.jpg";
  import edgar from "$lib/images/contributor/edgar.png";
  const contributors = [
    {
      photo: edzel,
      name: "Angeles, Edzel John",
      age: 23,
      course: "BSIT NW3A",
      address: "Samal Bataan",
    },
    {
      photo: meryliza,
      name: "Pabiton, Meryliza T.",
      age: 20,
      course: "BSIT NW3A",
      address: "Samal Bataan",
    },
    {
      photo: dannel,
      name: "Ramos, Dannel",
      age: 21,
      course: "BSIT NW3A",
      address: "Balanga Bataan",
    },
    {
      photo: edgar,
      name: "Tesoro, Edgar Z.",
      age: 20,
      course: "BSIT NW3A",
      address: "Bagac Bataan",
    },
  ];
</script>

<ul>
  {#each contributors as contributor}
    <li>
      <img draggable="false" src={contributor.photo} alt={contributor.name} />
      <p>{contributor.name}</p>
      <p>{contributor.age} years old</p>
      <p>{contributor.course}</p>
      <p>{contributor.address}</p>
    </li>
  {/each}
</ul>

<style>
  ul {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    height: calc(100vh - 25px);
  }
  ul > li {
    background: white;
    border-radius: 20px;
    user-select: none;
    cursor: pointer;
    text-align: center;
    color: gray;
    font-weight: bold;
    list-style: none;
    position: relative;
    padding: 25px 50px;
    padding-top: 100px;
    box-shadow:
      rgba(0, 0, 0, 0.25) 0px 14px 28px,
      rgba(0, 0, 0, 0.22) 0px 10px 10px;
  }
  ul > li > img {
    border-radius: 50%;
    box-shadow:
      rgba(0, 0, 0, 0.16) 0px 3px 6px,
      rgba(0, 0, 0, 0.23) 0px 3px 6px;
    width: 128px;
    border: 8px solid #9400ff;
    height: 128px;
    top: 0;
    left: 50%;
    transform: translate(-50%, -50%);
    position: absolute;
  }
  ul > li > p {
    margin-block: 5px;
  }
</style>
