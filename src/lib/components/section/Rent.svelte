<script>
    import {rents} from "$lib/stores/rent.js";
</script>

<section class="rents" id="rents">
    {#each rents as rent}
        <div class="rent-card">
            <img src={rent.image} alt={rent.description}/>
            <h3>{rent.price}</h3>
            <p class="truncate">{rent.description}</p>
            <p class="pb-4">{rent.address}</p>
            <button>Подробнее</button>
        </div>
    {/each}
</section>

<style lang="scss">
  .rents {
    @apply lg:grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
  }

  .rent-card {
    border: 1px solid #ccc;
    padding: 1rem;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  .rent-card img {
    width: 100%;
    max-height: 15rem;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 1rem;
  }

  .rent-card h3 {
    font-weight: bold;
    font-size: 1.2em;
    margin-bottom: 1rem;
  }

  .rent-card p {
    margin-bottom: 0.5rem;
  }

  .rent-card button {
    @apply rounded-xl;
    background-color: var(--red);
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
</style>