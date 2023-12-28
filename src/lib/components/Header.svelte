<script lang="ts">
    import MenuButton from "$lib/components/MenuButton.svelte";
    import logo from '$lib/images/logo-white.svg';

    let open: boolean;
    $: open = false;
</script>

<header class="px-12 py-6">
    <div>
        <a class="flex gap-2 items-center" href="/">
            <img alt="HomeBlocks Logo" class="w-7" src="{logo}">
            <b>HomeBlocks</b>
        </a>
    </div>

    <nav class="w-100 px-10 hidden lg:block">
        <ul class="flex gap-10">
            <li><a href="/">Квартиры</a></li>
            <li><a href="/houses">Дома</a></li>
            <li><a href="/rent">Аренда</a></li>
        </ul>
    </nav>

    <div class="menu flex items-center lg:hidden">
        <MenuButton/>
    </div>
</header>

<style lang="scss">
  header {
    position: fixed;
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    background-color: var(--header-background);
    height: var(--header-height);
    color: var(--header-text);
    z-index: 10;
  }
</style>
