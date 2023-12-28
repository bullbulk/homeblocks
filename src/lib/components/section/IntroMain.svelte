<script>
  import banner from "$lib/images/banner.png";
</script>

<section class="intro" id="intro">
    <div class="flex flex-col-reverse xl:grid h-full grid-cols-4 gap-8 xl:gap-20 items-center">
        <p class="intro-text text-xl">
            <b style="color: var(--red); font-size: 1.2em">HomeBlocks</b> - агентство недвижимости, специализирующееся на предоставлении своим клиентам услуг по покупке,
            продаже и аренде недвижимости. Мы работаем с различными типами недвижимости, включая жилые, коммерческие и
            инвестиционные объекты. Наша команда опытных агентов обладает глубокими знаниями рынка недвижимости и всегда
            готова помочь своим клиентам в сделке, от начала поиска подходящего объекта до успешного заключения сделки.
            Мы стремимся предоставить нашим клиентам самое качественное обслуживание, превосходящее их ожидания. Наша
            миссия - помочь клиентам осуществить свою мечту о приобретении идеального дома или успешном бизнесе.
        </p>
        <div class="banner">
            <img alt="HomeBlocks banner" class="rounded-xl" src="{banner}">
        </div>
    </div>
</section>

<style lang="scss">
  .intro {
    margin-top: var(--header-height);
  }

  .intro-text {
    grid-column: 1/3;
  }

  .banner {
    grid-column: 3/5;
    display: flex;
  }

  .banner img {
    max-height: 100%;
    max-width: 100%;
  }
</style>