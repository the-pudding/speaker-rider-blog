<script>
    import copy from "../data/copy.json";
    import wordmark from "../svg/pudding/wordmark.svg";
</script>

<section id="backstory">
    <h2>{copy.backstoryHed}</h2>
    <p class="credit">{@html copy.backstoryCredit}</p>
    {#each copy.backstoryText as backstoryText}
        <p>{@html backstoryText.value}</p>
    {/each}
    {#each copy.acknowledgments as acknowledgments}
        <p class='acknowledgements'>{@html acknowledgments.value}</p>
    {/each}
</section>

<style>
    #backstory {
        max-width: 40rem;
        margin: 0 auto 10rem auto;
        padding: 0 1rem;
    }

    h2 {
        font-family: var(--serif-hed);
        font-weight: 700;
        padding: 1rem 0 0 0;
        font-size: 2.25rem;
        border-top: 1px solid var(--gray-light);
        margin: 4rem 0 0 0;
    }

    p {
        font-family: var(--serif);
        font-size: 1.15rem; 
        line-height: 1.5;
        padding: 0.5rem 0;
    }

    .credit {
        color: var(--gray-dark);
        font-family: var(--sans);
    }

    .acknowledgements{
        font-family: var(--sans);
        color: var(--gray-dark);
        font-size: 1rem;
        font-style: italic;
        border-top: 1px solid var(--gray-light);
        margin: 2rem 0 0 0;
        padding: 1rem 0 0 0; 
    }

    @media only screen and (max-width: 620px) {
        h2 {
            font-size: 1.75rem;
        }

        .acknowledgements {
            font-size: 0.75rem;
        }
    }

    @media only screen and (max-width: 480px) {
        h2 {
            font-size: 1.5rem;
        }

        p {
            font-size: 1rem;
        }
    }
</style>