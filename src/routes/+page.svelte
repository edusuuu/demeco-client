<script>
  import logo from "$lib/images/logo.png";
  import facebook from "$lib/images/social/facebook.svg";
  import instagram from "$lib/images/social/instagram.svg";
  import regular from "$lib/images/fuels/regular.svg";
  import unleaded from "$lib/images/fuels/unleaded.svg";
  import diesel from "$lib/images/fuels/diesel.svg";
  import x from "$lib/images/social/x.svg";
  import Contributors from "../components/Contributors.svelte";
</script>

<div>
  <section id="home" class="section one">
    <div class="column container">
      <div class="left container">
        <h1>DEME CO</h1>
        <hr />
        <h2>online fuel delivery</h2>
        <a class="button" href="/signin">log in</a>
        <a class="signup-now" href="/signup">New Here? Sign Up now</a>
      </div>
      <div class="right container">
        <div class="left">
          <p>we'll drive you there</p>
          <p>we'll fuel your tomorrows</p>
          <p>we'll fuel your future</p>
        </div>
        <div class="right">
          <img draggable="false" src={logo} alt="logo" />
        </div>
      </div>
    </div>
    <p>
      A Web-based Online Fuel Ordering and Delivery System designed with the
      specific goal of helping people who ran out of gas in the middle of their
      trip, and make it available to everyone with an Internet connection
      wherever. And will also give it to them quickly. The application is
      intended to make obtaining fuel easier and more efficient. Customers can
      order fuel online and have it delivered to their home or office using this
      web-based technology. By providing a web-based ordering system that
      eliminates the inconveniences associated with old methods, our project
      intends to transform how individuals and companies source fuel.
    </p>
    <div class="socials">
      <img src={facebook} alt="facebook" />
      <img src={instagram} alt="instagram" />
      <img src={x} alt="x" />
    </div>
  </section>
  <section id="products" class="section two">
    <div class="fuels">
      <button>
        <img draggable="false" src={regular} alt="regular" />
      </button>
      <button>
        <img draggable="false" src={unleaded} alt="unleaded" />
      </button>
      <button>
        <img draggable="false" src={diesel} alt="diesel" />
      </button>
    </div>
  </section>
  <section id="about-us" class="section three">
    <Contributors />
  </section>
</div>

<style>
  div {
    margin-top: 25px;
  }
  div > section {
    min-height: calc(100vh - 25px);
    position: relative;
  }

  div > .section.one > .column.container {
    display: flex;
  }
  div > .section.one > p {
    margin-top: 100px;
    padding: 100px;
    font-size: 20px;
    color: white;
  }
  div > .section.one > .socials {
    text-align: center;
    position: absolute;
    bottom: 20;
    margin-top: 50px;
    left: 50%;
    transform: translateX(-50%);
  }
  div > .section.one > .socials > img {
    transform: scale(2);
    margin-inline: 20px;
    cursor: pointer;
  }
  div > .section.one > .column.container > .container {
  }
  div > .section.one > .column.container > .left.container {
    flex-basis: 40%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
  }
  div > .section.one > .column.container > .left.container h1 {
    font-size: 50px;
    font-weight: bold;
    text-wrap: none;
  }
  div > .section.one > .column.container > .left.container > hr {
    width: 60%;
    height: 8px;
    margin-block: 5px;
    background: white;
    outline: none;
    border: none;
  }
  div > .section.one > .column.container > .left.container > h2 {
    font-size: 30px;
    font-weight: lighter;
    text-transform: uppercase;
  }
  div > .section.one > .column.container > .left.container > a.button {
    font-size: 20px;
    text-transform: uppercase;
    padding: 10px 20px;
    background: white;
    border-radius: 20px;
    text-decoration: none;
    font-weight: bold;
    margin-top: 20px;
    box-shadow:
      rgba(0, 0, 0, 0.25) 0px 14px 28px,
      rgba(0, 0, 0, 0.22) 0px 10px 10px;
    color: none;
  }
  div > .section.one > .column.container > .left.container > a.button:hover {
    background: #371d50;
    color: white;
  }
  div > .section.one > .column.container > .left.container > a.signup-now {
    margin-top: 40px;
    color: white;
  }
  div > .section.one > .column.container > .right.container {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-basis: 60%;
  }
  div > .section.one > .column.container > .right.container > .left > p {
    text-transform: uppercase;
    font-size: 30px;
    font-weight: bold;
    text-wrap: nowrap;
    color: white;
  }
  div > .section.one > .column.container > .right.container > .right {
    max-width: 400px;
    margin-left: 20px;
  }
  div > .section.one > .column.container > .right.container > .right > img {
    object-fit: cover;
    width: 100%;
  }

  div > .section.two > .fuels {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    height: calc(100vh - 25px);
  }
  div > .section.two > .fuels > button {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    padding: 40px;
    border: none;
    outline: none;
    cursor: pointer;
    transition: transform 250ms ease;
    position: relative;
  }
  div > .section.two > .fuels > button:active {
    transform: scale(0.9);
    background: linear-gradient(rgb(255, 255, 255), transparent),
      linear-gradient(to top left, rgb(189, 95, 198), transparent),
      linear-gradient(to top right, rgb(158, 123, 228), transparent);
    background-blend-mode: screen;
  }
  div > .section.two > .fuels > button:nth-child(1)::before {
    content: "regular";
    position: absolute;
    text-transform: uppercase;
    left: 50%;
    transform: translateX(-50%);
    bottom: -40px;
    color: white;
    font-size: 20px;
    font-weight: bold;
  }
  div > .section.two > .fuels > button:nth-child(2)::before {
    content: "unleaded";
    position: absolute;
    text-transform: uppercase;
    left: 50%;
    transform: translateX(-50%);
    bottom: -40px;
    color: white;
    font-size: 20px;
    font-weight: bold;
  }
  div > .section.two > .fuels > button:nth-child(3)::before {
    content: "diesel";
    position: absolute;
    text-transform: uppercase;
    left: 50%;
    transform: translateX(-50%);
    bottom: -40px;
    color: white;
    font-size: 20px;
    font-weight: bold;
  }
  div > .section.two > .fuels > button > img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
  }
</style>
