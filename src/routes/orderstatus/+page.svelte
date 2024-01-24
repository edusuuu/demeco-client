<script>
import icon1 from "$lib/images/shipping/ship1.png";
import icon2 from "$lib/images/shipping/ship2.png";
import icon3 from "$lib/images/shipping/ship3.png";
import icon4 from "$lib/images/shipping/ship4.png";
</script>
<div class="container">
    <div class="details">
      <div class="order">
        <h1> Order <span> Status </span></h1>
        </div>
        <div class="date">
          <p> Expected Arrival 01/25/2024</p>
          <p> USPS <b> 0123456789 </p>
        </div>
    </div>

    <div class="track">
      <ul id="progress" class="text-center">
      <li class="active"> </li>
      <li class="active"> </li>
      <li class="active"> </li>
      <li class="active"> </li>
      </ul>
  </div>

  <div class="lists">
    <div class="list">
      <img src={icon1} alt="1st">
      <p> Order <br> Processed </p>
    </div>

    <div class="lists">
      <div class="list">
        <img src={icon2} alt="2nd">
        <p> Order <br> Shipped </p>
      </div>

      <div class="lists">
        <div class="list">
          <img src={icon3} alt="3rd">
          <p> Order <br> Enroute </p>
        </div>

        <div class="lists">
          <div class="list">
            <img src={icon4} alt="4th">
            <p> Order <br> Arrived </p>
          </div>
          </div>
  </div>
</div>
</div>
</div>

  <style>
    :root {
  --cont: #eceff1;
  --line: #8a1dff;
  --txt: #824db4;
  --light: #c5cae9;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.bg {
  min-height: 100vh;
  font-family: Arial, Helvetica, sans-serif;
}


.container {
  width: 1100px;
  max-width: 100%;
  margin-top: 100px;
  border-radius: 20px;
  padding: 40px;
  background: var(--cont);
  position: relative;
  border: #8a1dff;
  border-style: solid;
  border-width: 4px;
  opacity: 0;
  transform: translateY(30px);
  animation: moveup 0.5s linear forwards;
margin-left: 7%;
}
@keyframes moveup {
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}

.details {
  display: flex;
  gap: 1em;
  flex-wrap: wrap;
  justify-content: space-between;
}

.order h1 {
  text-transform: uppercase;
}

.order span {
  color: var(--txt);
}

.date p {
  font-size: 1.1rem;
}

.track {
  margin: 4em 0 8em;
}

#progress {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  gap: 1em;
  position: relative;
  text-align: center;
}

#progress li {
  width: 20%;
  position: relative;
}

#progress li::before {
  content: "\2713";
  position: absolute;
  display: flex;
  justify-content: center;
  width: 50px;
  align-items: center;
  font-size: 2rem;
  height: 50px;
  background: var(--line);
  color: #fff;
  border-radius: 50%;
  z-index: 11111;
}

#progress li:last-child::before {
  content: "\2713";
  font-weight: bold;
  background: var(--light);
}

#progress::before {
  content: "";
  position: absolute;
  top: 20px;
  width: 55%;
  margin-left: 35px;
  height: 10px;
  background: var(--line);
  z-index: 111;
}

#progress::after {
  content: "";
  position: absolute;
  top: 20px;
  width: 80%;
  height: 10px;
  background: #c5cae9;
}

.lists {
  display: flex;
  gap: 7.5em;
  flex-wrap: wrap;
  align-items: center;
}

.list {
  display: flex;
  gap: 1em;
  margin-bottom: 20px;
  flex-wrap: 1 1 50px;
}
.list img {
  width: 50px;
}

.list p {
  font-size: 1.1rem;
}

  </style>