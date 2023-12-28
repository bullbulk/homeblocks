<script>
    import '$lib/css/styles.scss';
    import Intro from "$lib/components/section/IntroMain.svelte";
    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/section/Footer.svelte";
</script>


<div id="page">
    <Header/>

    <main>
        <slot/>
    </main>

    <Footer/>
</div>
