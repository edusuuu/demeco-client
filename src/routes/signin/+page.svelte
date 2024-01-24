<script>
  import logo from "$lib/images/logo.png"
</script>

<div class="page">
  <form>
    <div>
      <img draggable="false" src={logo} alt="logo">
    </div>
    <h1>Welcome!</h1>
    <p>Sign in to your account.</p>
    <input type="text" placeholder="email" />
    <input type="password" placeholder="password" />
    <a href="/password/forgot">Forgot Password</a>
    <button type="submit">sign in</button>
  </form>
</div>

<style>
  .page {
    min-height: 100vh;
    margin-top: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .page > form > div {
    width: 128px;
    height: 128px;
  }
  .page > form > div > img {
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
  .page > form {
    display: flex;
    margin-inline: auto;
    width: 600px;
    padding-block: 50px;
    border-radius: 2rem;
    outline: 2px solid #a59bd5;
    background: #a59bd5;
    box-shadow:
      rgba(165, 155, 213, 0.16) 0px 3px 6px,
      rgba(165, 155, 213, 0.23) 0px 3px 6px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
  }

  .page > form > a {
    color: black;
  }
  .page > form > button {
    padding: 10px 20px;
    background: #371d50;
    border-radius: 15px;
    font-size: 20px;
    font-weight: bold;
    cursor: pointer;
    border: none;
    color: #a59bd5;
  }
  .page > form > button:active {
    transform: scale(0.9);
  }

  .page > form > input {
    padding: 10px 20px;
    border-radius: 5px;
    width: 70%;
    background: #d3b5f0;
    color: black;
    opacity: 0.75;
    border: none;
    outline: none;
    font-size: 20px;
  }
  .page > form > input::placeholder {
    color: black;
  }
</style>
