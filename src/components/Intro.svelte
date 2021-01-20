<script>
    import copy from "../data/copy.json";
</script>

<section id="intro">
    <h1>{copy.hed}</h1>
    <h2>{copy.dek}</h2>
    <div class="collab">
        <p class="credit">{@html copy.credit}</p>
        <a href="https://opennews.org/" target=_blank>
            <img alt="open news logo" src="assets/images/open-news-2017.png" />
        </a>
    </div>
    {#each copy.intro as intro}
        <p>{@html intro.value}</p>
    {/each}
    <a class="refer" href="https://opennews.org/speaker-rider" target=_blank>{@html copy.riderLink}</a>
</section>

<style>
    #intro {
        max-width: 52rem;
        margin: 0 auto;
        padding: 1rem 1rem 0 1rem;
    }

    h1 {
        font-family: var(--serif-hed);
        font-size: 4em;
        line-height: 1;
        padding: 0 0;
        text-align: center;
        font-weight: 900;
    }

    h2 {
        text-align: center;
        max-width: 40rem;
        margin: 0 auto; 
        padding: 0 0 3rem 0; 
    }

    .collab {
        max-width: 32rem;
        margin: 0 auto 3rem auto;
        border-top: 1px solid var(--gray-light);
        border-bottom: 1px solid var(--gray-light);
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        padding: 1rem 0;
    }
    
    .collab a {
        background-image: none;
    }

    .credit {
        font-family: var(--sans);
        color: var(--gray-dark);
        font-size: 1rem;
        font-style: italic;
        padding: 0 0.5rem 0 0;
        margin: 0;
    }

    .collab img {
        max-width: 8rem;
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
        color: var(--off-white);
        font-size: 1.25rem;
        text-decoration: none;
        padding: 0.75rem 1rem;
        border-radius: 0.25rem;
        background-position: 0 0em;
        position: relative;
        background-color: var(--purple);
        background-image: none;
    }

    .refer:hover {
        background-color: #9A32C1;
    }

    .refer::after {
        position: absolute;
        content: "";
        display: inline-block;
        height: 100%;
        width: 100%;
        border-radius: 0.25rem;
        top: 0;
        left: 0;
        z-index: -1;
        transition: all .4s;
        background-color: var(--gray-light);
    }

    .refer:hover::after {
        transform: scaleX(1.2) scaleY(1.6);
        opacity: 0;
    }

    @media only screen and (max-width: 660px) {
        h1 {
            font-size: 3rem;
            padding: 0 0 1rem 0;
        }
    }

    @media only screen and (max-width: 500px) {
        h1 {
            font-size: 2rem;
        }

        h2 {
            font-size: 1rem;
            padding: 0 0 2rem 0;
        }
        
        p {
            font-size: 1rem;
        }

        .refer {
            font-size: 1rem;
            max-width: 12rem;
        }

        .collab {
            flex-direction: column;
            max-width: 20rem;
            margin: 0 auto 2rem auto;
        }

        .credit {
            font-size: 0.75rem;
            padding: 0 0 0.5rem 0;
        }
    }
</style>