<script>
    import copy from "../data/copy.json";
</script>

<section id="intro">
    <h1>{copy.hed}</h1>
    {#each copy.intro as intro}
        <p>{@html intro.value}</p>
    {/each}
</section>

<style>
    #intro {
        max-width: 50rem;
        margin: 0 auto;
        padding: 2rem 0 0 0;
    }

    h1 {
        font-family: var(--serif-hed);
        font-size: 4em;
        line-height: 1;
        padding: 0 0 2rem 0;
        text-align: center;
        font-weight: 700;
    }

    p {
        font-family: var(--serif);
        max-width: 40rem;
        margin: 0 auto;
        font-size: 1.15rem; 
        line-height: 1.5;
        padding: 0.5rem 0;
    }
</style>