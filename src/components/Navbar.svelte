<nav>
  <ul>
    <li>
      <a href="/#home">home</a>
    </li>
    <li>
      <a href="/#products">products</a>
    </li>
    <li>
      <a href="/#about-us">about us</a>
    </li>
    <li>
      <a href="/signin">sign in</a>
    </li>
  </ul>
</nav>

<style>
  nav {
    position: sticky;
    top: 25px;
    z-index: 999;
  }
  nav > ul {
    display: flex;
    background: #371d50;
    align-items: center;
    width: 95vw;
    margin-inline: auto;
    border-radius: 25px;
    outline: 2px solid #a59bd5;
    overflow: hidden;
    z-index: 999;
    position: relative;
  }
  nav > ul > li {
    list-style: none;
  }
  nav > ul > li:hover {
    background: #a59bd5;
  }
  nav > ul > li:hover > a {
    color: #371d50;
  }
  nav > ul > li:last-child {
    position: absolute;
    right: 0;
  }
  nav > ul > li > a {
    display: block;
    text-decoration: none;
    color: #fff;
    font-weight: bold;
    padding: 20px;
    text-transform: uppercase;
    text-wrap: nowrap;
  }
</style>
