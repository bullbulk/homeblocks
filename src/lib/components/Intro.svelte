<section class="intro" id="intro">
    <h1>This is a Svelte template site</h1>
    <button class="absolute text-center left-0 right-0 p-20 bottom-5 lg:bottom-15"
            on:click={function() {
                document.getElementById('about-me')?.scrollIntoView(
                    {behavior: 'smooth', block: 'start', inline: 'nearest'}
                    );
            }}>
        <i class="text-gray-500 text-xl fa-solid fa-arrow-down"></i>
    </button>
</section>

<style lang="scss">
  .intro {
    @apply p-0;

    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
  }
</style>
