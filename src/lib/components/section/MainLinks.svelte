<section class="main-links" id="main-links">
    <a href="/#flats">Квартиры</a>
    <a href="/houses">Дома</a>
    <a href="/rent">Аренда помещений</a>
</section>

<style lang="scss">
  .main-links {
    @apply flex justify-center gap-5 pt-0;

     & a {
       @apply text-lg rounded-xl;
       color: white;
       padding: 0.5rem 1rem;
       background-color: var(--red);
     }
  }
</style>