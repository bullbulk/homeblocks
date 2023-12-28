<script>
    import {houses} from "$lib/stores/houses.js";
</script>

<section class="houses" id="houses">
    {#each houses as house}
        <div class="house-card">
            <img src={house.image} alt={house.description}/>
            <h3>{house.price}</h3>
            <p class="truncate">{house.description}</p>
            <p class="pb-4">{house.address}</p>
            <button>Подробнее</button>
        </div>
    {/each}
</section>

<style lang="scss">
  .houses {
    @apply lg:grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
  }

  .house-card {
    border: 1px solid #ccc;
    padding: 1rem;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  .house-card img {
    width: 100%;
    max-height: 15rem;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 1rem;
  }

  .house-card h3 {
    font-weight: bold;
    font-size: 1.2em;
    margin-bottom: 1rem;
  }

  .house-card p {
    margin-bottom: 0.5rem;
  }

  .house-card button {
    @apply rounded-xl;
    background-color: var(--red);
    color: white;
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
</style>