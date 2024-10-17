<script>
  function toggleMenu() {
    const menu = document.getElementById("nav-menu");
    menu.classList.toggle("active");
  }
</script>

<header>
  <div class="logo">
    <img src="/logo.png" alt="SlovContact Logo" />
  </div>
  <nav>
    <button class="hamburger" on:click={toggleMenu}>&#9776;</button>
    <ul id="nav-menu">
      <li><a href="/">Domov</a></li>
      <li><a href="/history">História firmy</a></li>
      <li><a href="/contact">Kontakt</a></li>
    </ul>
  </nav>
</header>

<nav style="display: none;">
  <ul class="active"></ul>
</nav>

<style>
  header {
    background-color: #1a3c6e;
    color: white;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    display: flex;
    align-items: center;
  }

  .logo img {
    height: 50px;
    margin-right: 10px;
  }

  nav {
    position: relative;
    height: 60px;
  }

  nav .hamburger {
    display: none;
    font-size: 24px;
    cursor: pointer;
  }

  nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
  }

  nav li {
    margin-left: 1rem;
  }

  nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
  }

  nav a:hover {
    text-decoration: underline;
  }

  @media (max-width: 768px) {
    nav .hamburger {
      display: block;
    }

    nav ul {
      display: none;
      flex-direction: column;
      position: fixed;
      background-color: #1a3c6e;
      top: 80px;
      left: 0 !important;
      width: 100vw;
      z-index: 1;
    }

    nav ul.active {
      display: flex;
    }

    nav li {
      margin: 0.5rem 0;
      margin-left: 0; /* Reset margin for vertical layout */
    }
  }
</style>
