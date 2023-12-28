<script>
    import {flats} from "$lib/stores/data.js";
</script>

<section class="flats" id="flats">
    {#each flats as flat}
        <div class="flat-card">
            <img src={flat.image} alt={flat.title}/>
            <h3>{flat.price}</h3>
            <p class="truncate">{flat.description}</p>
            <p class="pb-4">{flat.address}</p>
            <button>Подробнее</button>
        </div>
    {/each}
</section>

<style lang="scss">
  .flats {
    @apply lg:grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
  }

  .flat-card {
    border: 1px solid #ccc;
    padding: 1rem;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  .flat-card img {
    width: 100%;
    max-height: 15rem;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 1rem;
  }

  .flat-card h3 {
    font-weight: bold;
    font-size: 1.2em;
    margin-bottom: 1rem;
  }

  .flat-card p {
    margin-bottom: 0.5rem;
  }

  .flat-card button {
    @apply rounded-xl;
    background-color: var(--red);
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
</style>