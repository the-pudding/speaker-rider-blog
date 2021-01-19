<script>
    import copy from "../data/copy.json";
</script>

<section id="intro">
    <h1>{copy.hed}</h1>
    <h2>{copy.dek}</h2>
    <p class="credit">{@html copy.credit}</p>
    {#each copy.intro as intro}
        <p>{@html intro.value}</p>
    {/each}
    <a class="refer" href="https://opennews.org/speaker-rider4" target=_blank>{@html copy.riderLink}</a>
</section>

<style>
    #intro {
        max-width: 55rem;
        margin: 0 auto;
        padding: 1rem 1rem 0 1rem;
    }

    h1 {
        font-family: var(--serif-hed);
        font-size: 4em;
        line-height: 1;
        padding: 0 0;
        text-align: center;
        font-weight: 700;
    }

    h2 {
        text-align: center;
        max-width: 40rem;
        margin: 0 auto; 
        padding: 0 0 3rem 0; 
    }

    .credit {
        font-family: var(--sans);
        max-width: 30rem;
        color: var(--gray-dark);
        font-size: 1rem;
        text-align: center;
        font-style: italic;
        padding: 1rem 0; 
        margin-bottom: 3rem;
        border-top: 1px solid var(--gray-light);
        border-bottom: 1px solid var(--gray-light);
    }

    p {
        font-family: var(--serif);
        max-width: 40rem;
        margin: 0 auto;
        font-size: 1.15rem; 
        line-height: 1.5;
        padding: 0.5rem 0;
    }

    .refer {
        margin: 2rem auto 4rem auto;
        max-width: 16rem;
        display: flex;
        justify-content: center;
        align-self: center;
        background-color: var(--purple);
        color: var(--white);
        font-size: 1.25rem;
        text-decoration: none;
        padding: 0.75rem 1rem;
        border-radius: 0.25rem;
    }

    .refer:hover {
        background-color: var(--gray-dark);
    }

    @media only screen and (max-width: 620px) {
        h1 {
            font-size: 3rem;
            padding: 0 0 1rem 0;
        }
    }

    @media only screen and (max-width: 480px) {
        h1 {
            font-size: 2rem;
        }

        h2 {
            font-size: 1.25rem;
            padding: 0 0 2rem 0;
        }
        
        p {
            font-size: 1rem;
        }

        .refer {
            font-size: 1rem;
            max-width: 12rem;
        }
    }
</style>