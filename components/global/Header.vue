<template>
  <nav class="navbar navbar-expand-lg navbar-togglable fixed-top navbar-light ">
    <div class="container">
      <a to="/" class="navbar-brand d-lg-none shadow rounded p-2 back-color">Happy Klang / Jeannette Britz</a>
      <button class="navbar-toggler back-color" type="button" data-bs-toggle="collapse" data-bs-target="#navbarCollapse"
        aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse shadow rounded p-2 back-color" id="navbarCollapse">
        <ul class="navbar-nav ">

          <li class="nav-item">
            <a class="nav-link " routerLinkActive="selected" routerLink="/klangReisen"
              style="color: black">Klangreisen</a>
          </li>
          <li class="nav-item">
            <a class="nav-link " routerLinkActive="selected" routerLink="/klangMassagen"
              style="color: black">Klangmassagen</a>
          </li>
          <li class="nav-item">
            <a class="nav-link " routerLinkActive="selected" routerLink="/kinderKlang"
              style="color: black">Kinder-Klang</a>
          </li>
        </ul>
        <div class=" navbar-brand d-none d-lg-flex mx-lg-auto" style="color: black" routerLink="/home">
          <ul class="navbar-nav ">
            <li class="nav-item">
              <img src="../../assets/img/logo.jpeg" alt="Error" class="rounded-circle" style=" width: 40px; " />
            </li>
            <li class="nav-item">
              <a class="nav-link mt-1" routerLink="/kinderKlang" style="color: black">Jeannette Britz</a>
            </li>
          </ul>
        </div>
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link " routerLinkActive="selected" routerLink="/seminare" style="color: black">Workshops</a>
          </li>
          <li class="nav-item">
            <a class="nav-link " routerLinkActive="selected" routerLink="/produkte" style="color: black">Webshop /
              Honorar</a>
          </li>
          <li class="nav-item">
            <a class="nav-link wht" routerLinkActive="selected" routerLink="/ueberMich" style="color: black">Über
              mich</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style>
html {
  block-size: 100%;
  inline-size: 100%;
}

body {
  min-block-size: 100%;
  min-inline-size: 100%;
  margin: 0;
  box-sizing: border-box;
  display: grid;
  place-content: center;
  font-family: system-ui, sans-serif;
}

@media (orientation: landscape) {
  body {
    grid-auto-flow: column;
  }
}

.back-color {
  background-color: white !important;
  z-index: 1;
}
</style>

<script>
export default {
  name: 'Header'
}
</script>

