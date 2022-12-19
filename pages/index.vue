<template>
  <main style="padding: 1rem; text-align: center">
    <div>
      <div style="margin-top: 5rem">
        <p style="text-align: center; font-size: 30pt">
          <span>Herzlich Willkommen!</span>
        </p>
        <!-- <p style="text-align: center;  font-size:30pt; "><span >Willkommen!</span></p> -->
        <img src="assets/img/logo.jpeg" alt="Error" class="rounded-circle" style="width: 350px; margin-bottom: 2rem" />
      </div>
    </div>
    <div class="container col-md-5 margin padding rounded shadow-lg modal-style" style="font-size: 15pt">
      <h1 class="pb-2 border-bottom">Anstehende Termine</h1>
      <div>
        <posts post-type="termine" :amount="10" />
      </div>
      <p>
        19:00 Uhr - 20:00 Uhr <br />Klangreise in der Praxis Lebensfit
        (Hohenzollernstr. 119; 56068 Koblenz)
      </p>
    </div>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts;
    try {
      posts = await $content("termine").fetch();
    } catch (e) {
      error({ message: "Keine anstehenden Termine" });
    }
    return { posts };
  },
}
</script>