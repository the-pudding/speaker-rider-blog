<script>
    import copy from "../data/copy.json";
</script>

<section id="speakers">
    <h2>{copy.speakerHed}</h2>
    {#each copy.speakerText as speakerText}
        <p>{@html speakerText.value}</p>
    {/each}

    <h3>{copy.emailHed}</h3>
    <div class="email">
        {#each copy.email as email}
            <p>{@html email.value}</p>
        {/each} 
    </div>

    <h3>{copy.additionalHed}</h3>
    <ul>
        {#each copy.additionalThings as additionalThings}
        <li>
            <span>{additionalThings.hed}</span>
            {@html additionalThings.text}
        </li>
        {/each} 
    </ul>

    <h3>{copy.newSpeakerHed}</h3>
    {#each copy.newSpeakerText as newSpeakerText}
        <p>{@html newSpeakerText.value}</p>
    {/each} 
    <ul>
        {#each copy.newSpeakerThings as newSpeakerThings}
        <li>
            <span>{newSpeakerThings.hed}</span>
            {@html newSpeakerThings.text}
        </li>
        {/each} 
    </ul>
</section>

<style>
    #speakers {
        max-width: 40rem;
        margin: 0 auto;
    }

    h2 {
        font-family: var(--serif-hed);
        font-weight: 700;
        padding: 2rem 0 0 0;
        font-size: 2.25rem;
    }

    h3 {
        font-family: var(--serif-hed);
        font-weight: 700;
        padding: 2rem 0 0 0;
        font-size: 1.5rem;
    }

    p {
        font-family: var(--serif);
        font-size: 1.15rem; 
        line-height: 1.5;
        padding: 0.5rem 0;
    }
    
    .email {
        background-color: var(--white);
        padding: 1rem 2rem;
        border-radius: 0.25rem;
        border: 1px solid var(--gray-light);
        box-shadow: 0.25rem 0.25rem 1rem rgba(var(--gray-light), 0.5);
    }

    .email p {
        font-family: var(--sans);
    }

    ul {
        font-family: var(--serif);
        font-size: 1.15rem; 
        line-height: 1.5;
    }

    li {
        padding: 1rem 0; 
    }

    li span {
        font-family: var(--serif);
        font-weight: 700;
    }

    .insert {
        font-weight: 700;
    }
</style>