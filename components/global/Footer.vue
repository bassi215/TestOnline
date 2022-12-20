<template>
    <footer class="rounded d-flex flex-wrap justify-content-between align-items-center my-0  border-top">
        <p class=" mb-0 text-muted">© 2022 Happy Klang</p>
        <ul class="nav  justify-content-end">
            <li class="nav-item">
                <a routerLink="/home" class="nav-link text-muted">Home</a>
            </li>
            <li class="nav-item">
                <a href="#" style="color: black" class="nav-link text-muted" v-b-modal.modal-center>Kontakt</a>
                <b-modal id="modal-center" centered title="Kontakt">
                    <Kontakt></Kontakt>
                </b-modal>
            </li>
            <li class="nav-item">
                <a routerLink="/impressum" class="nav-link text-muted">Impressum</a>
            </li>
            <li class="nav-item">
                <a routerLink="/datenschutz" class="nav-link text-muted">Datenschutz</a>
            </li>
        </ul>



    </footer>
</template>

<style>
a::before {
    transform: scaleX(0);
    transform-origin: bottom right;
}

a:hover::before {
    transform: scaleX(1);
    transform-origin: bottom left;
}

a::before {
    content: " ";
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    inset: 0 0 0 0;
    background: #44a6b4c4;
    z-index: -1;
    transition: transform 0.3s ease;
    border-radius: 0.375rem !important;
}

a {
    position: relative;
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
</style>

<script>
export default {
    name: 'Footer'
}
</script>